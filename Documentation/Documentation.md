# Pitch Dark

## Overview

**Pitch Dark** is a stealth-survival game set aboard a derelict, lightless spaceship. Players must navigate through shadows, manage scarce resources, avoid or confront adaptive AI threats, and complete evolving mission objectives. Emphasis is placed on immersive lighting, audio design, player vulnerability, and replayability through randomized elements. Developed using **Unreal Engine 5**, the project leverages Blueprints and C++ integration for modular system design.

---

## Table of Contents

1. [Player System](#player-system)
2. [Status System](#status-system)
3. [Level Design](#level-design)
4. [AI System](#ai-system)
5. [UI System](#ui-system)
6. [Core Game Loop](#core-game-loop)
7. [Immersion](#immersion)
8. [Unreal Engine Implementation Notes](#unreal-engine-implementation-notes)

---

## Player System

### Core Actions

| Action             | Implementation                                                                 |
|--------------------|----------------------------------------------------------------------------------|
| Basic Movement     | `CharacterMovementComponent`, mapped via `Enhanced Input System`                |
| Interact / Pickup  | `LineTraceByChannel` or `SphereTrace`, trigger interaction interface on hit     |
| Use Items          | Equip or consume via Inventory system → Interface to `ItemData` or gameplay tags |
| Weapon Handling    | Modular `WeaponComponent`, supports fire modes, noise emission, and durability   |
| Crouch / Lean      | Animation Blueprint + `Camera Offset`, `Capsule Half Height` adjustment          |

### Inventory & Equipment

- `InventoryComponent` stores items, dynamically updatable
- Each item defined by a `DataAsset` (weight, type, use function, stackability)
- Support for **hotbar**, **tool use cooldown**, and **context-sensitive prompts**

---

## Status System

| Feature              | Unreal Tool/Implementation                                                |
|----------------------|---------------------------------------------------------------------------|
| Health & Damage      | `ApplyDamage()`, `DamageType` subclasses, linked to `HealthComponent`    |
| Psychological Effects| Use `GameplayTag` or `GameplayEffect` for debuffs (e.g., panic, hallucination) |
| Noise/Stealth Value  | Custom "Sound Event" struct, passed to AI via `MakeNoise()` or interfaces |
| Lighting Awareness   | Player visibility scalar (0–1) determined by nearby dynamic lights         |

### Status UI Integration

- Flashing health when critically low
- Heartbeat or breathing audio cues based on stealth tension
- Screen vignette or chromatic aberration effects for low sanity/stamina

---

## Level Design

### Immersion & Mood

| Feature             | Implementation                                                            |
|----------------------|---------------------------------------------------------------------------|
| Visual Cohesion     | Use shared material library; modular environment kits                     |
| Audio Zones         | `Ambient Sound` actors & `Audio Volume` triggers for region-specific cues |
| Darkness Mechanics  | Dynamic lights (`Point`, `Spot`), flicker/timed decay via Timeline curves  |
| Environmental Events| Scripted via Level Blueprints or `LevelSequence` (e.g., sparks, hull groans) |

### Mission & Objectives

- **Escape Objective**: Activated via interaction with final console, tracked via `GameState`
- **Sub Objectives**: Modular system with `ObjectiveComponent` on actors; states: Inactive → Active → Complete
- **Dynamic World Events**: Randomized system triggers enemy patrols, environmental hazards, or alternate paths

---

## AI System

### Perception & Awareness

| Sense               | Tool/Logic                                           |
|----------------------|-----------------------------------------------------|
| Vision               | `AISense_Sight`, adjustable peripheral & range     |
| Hearing              | `AISense_Hearing`, linked to player `MakeNoise()`  |
| Memory / Tracking    | Use Blackboard timers to forget last known location |

### Behavior States

| State               | Trigger Logic                                                      |
|----------------------|-------------------------------------------------------------------|
| Idle/Patrol          | Random or predefined Waypoints; `BTTask_MoveTo`                   |
| Investigate          | Sound or brief visual detection; navigate to `LastHeardLocation` |
| Search               | Random walk within search radius; use `EQ System`                 |
| Chase                | Direct path to player, call reinforcements                        |
| Combat               | Attack player; if low health, fallback or trigger alarm           |

### AI Enhancements

- **Line-of-sight checks** enhanced with obstacle detection via `LineTrace`
- Memory system stores **last seen time**, **direction**, and **sound source tags**
- AI communicates via event dispatchers (e.g., "Intruder detected" → group response)

---

## UI System

| Element              | Description                                                              |
|----------------------|---------------------------------------------------------------------------|
| HUD                  | Health, equipped item, stealth status, and ammo (if applicable)           |
| Inventory            | UMG Widget with drag-drop, tooltips from `ItemDataAsset`                 |
| Objectives Tracker   | Lists active and completed objectives, supports localization              |
| Enemy Alert Indicator| On-screen UI pulses or warning text when player is spotted/heard         |
| Context Prompts      | Dynamic prompt widget triggered from `Interactable Interface` targets     |

---

## Core Game Loop

```
1. Player awakens in cryo chamber with no light.
2. Player finds flashlight, then explores and discovers objectives.
3. Encounters intelligent AI patrols or dynamic threats.
4. Completes critical objectives to unlock final escape route.
5. Either escapes or dies; data logged for session feedback.
```

### Loop Extensions

- Support for **roguelike structure**: randomized ship layouts, objective locations
- Implement **meta-progression**: logs found, data gathered, unlocks for future runs
- Optional **resource crafting system** (e.g., battery packs, makeshift weapons)

---

## Immersion

| Technique             | Implementation Detail                                                |
|------------------------|---------------------------------------------------------------------|
| Dynamic Soundscape     | Use layered sound cues, distance-based mixing via `Audio Volumes`  |
| Visual Feedback        | Post-processing effects, head-bob, camera shakes                   |
| Lighting Control       | Interactive lighting (e.g., power restoration, light-switch puzzles)|
| Haptics / Gamepad      | Rumble triggers during chase sequences or key discoveries          |
| Diegetic UI            | Use world-space interfaces (e.g., wrist display, terminals)         |

---

## Unreal Engine Implementation Notes

- **Project Structure**:
  - `/Core/Characters/`, `/Core/AI/`, `/Core/Items/`, `/Widgets/`, `/Blueprints/Utility/`
- **Blueprints & C++ Split**:
  - Core logic (AI, Inventory, Status) in C++
  - Quick iteration (UI, visual scripting) in Blueprints
- **Key Plugins**:
  - `Enhanced Input`
  - `Gameplay Tags`
  - `Environment Query System (EQS)`
  - `Modular Gameplay Features` (optional scalability)
