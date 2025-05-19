# Pitch Dark

## Overview

**Pitch Dark** is a stealth-survival game set aboard a dark, immersive spaceship. The player must navigate, complete objectives, and survive against intelligent AI threats. This document outlines the core gameplay systems and their integration using Unreal Engine components and tools.

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

| Action           | Implementation                         |
|------------------|----------------------------------------|
| Basic Movement   | `CharacterMovementComponent`, Input    |
| Pick Up Items    | `Actor` interaction, `Trace` or `Overlap` |
| Use Weapon       | `Actor Component`, projectile/spawn    |
| Use on Self      | Trigger effect via blueprint or animation |

---

## Status System

| Feature             | Unreal Implementation                            |
|----------------------|--------------------------------------------------|
| Take Damage          | `ApplyDamage()`, `Event AnyDamage`              |
| Pitch Effects        | Custom `GameplayEffect` or `Post Process Volume` |
| Stealth / Noise      | AI Perception – `StimuliSourceComponent`        |

- Noise generated with `MakeNoise()` or custom events
- Stealth state toggled through `Blackboard` values

---

## Level Design

### Immersion

| Feature               | Implementation                            |
|------------------------|-------------------------------------------|
| Visual Continuity      | Consistent meshes/materials in `Level`    |
| Good Visibility        | Carefully placed `Lights` & `Fog Volumes` |
| Dark Ambience          | `Post Processing`, low exposure, SFX      |

### Objectives

- **Main**: Escape the ship (tracked via `GameMode` or `ObjectiveManager`)
- **Sub**: Trigger generators, collect tools, unlock doors (`Blueprint Actors` + `Interface`)

Use `Trigger Volumes`, `Overlap Events`, or `Interactable` base classes.

---

## AI System

### Behavior

| Perception            | Unreal Tool                    |
|------------------------|--------------------------------|
| See Player             | `AI Perception → Sight`        |
| Hear Player            | `AI Perception → Hearing`      |
| Attack Player          | Behavior Tree tasks            |

### States

| State                 | Tool/Logic                                  |
|------------------------|---------------------------------------------|
| Patrol                | `Behavior Tree` with `Waypoint` system       |
| Alert / Search        | Use `Blackboard` key & perception events     |
| Lost Target           | Set timer to search then resume patrolling   |

---

## UI System

| UI Element           | Unreal Widget Blueprint (UMG)            |
|------------------------|------------------------------------------|
| Minimalist HUD        | Display ammo, health, objectives          |
| Health Display         | Bind to `PlayerHealthComponent`          |
| Weapon & Ammo          | Access from `Inventory` or weapon class  |
| Objective Tracker      | Bind to `ObjectiveManager`               |

---

## Core Game Loop

```text
1. Player explores the ship.
2. Objectives are revealed (randomized or ordered).
3. AI reacts to player actions (sight/noise).
4. Player survives to complete extraction.