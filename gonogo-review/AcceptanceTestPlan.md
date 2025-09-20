# **ACCEPTANCE TEST PLAN – PITCH DARK**

Pitch Dark is a multiplayer fps horror game in a sci-fi environment where players need to achieve tasks in order to complete missions and try to survive various dangers, such as enemies and the Pitch, a dangerous fog that needs to be avoided. The game targets players who enjoy sci-fi horror experiences, combining tense multiplayer action with atmospheric survival gameplay.

## Table of Contents
- [1. Test Objective](#1-test-objective)
    - [1.1 Global resume](#11-global-resume)
    - [1.2 Scope of testing](#12-scope-of-testing)
    - [1.3 Overview](#13-overview)
- [2. Assumptions/constraints](#2-assumptionsconstraints)
    - [2.1 Assumptions](#21-assumptions)
    - [2.2 Constraints](#22-constraints)
- [3. Known Issues & Limitations](#3-known-issues--limitations)
- [4. Software requierement](#4-software-requierement)
- [5. Environmental Needs](#5-environmental-needs)
- [6. Test scenarios](#6-test-scenarios)
    - [6.1 Main Menu](#61-main-menu)
    - [6.2 Settings Menu](#62-settings-menu)
    - [6.3 Lobby](#63-lobby)
    - [6.4 Player behaviour](#64-player-behaviour)
    - [6.5 AI Behaviour](#65-ai-behaviour)
    - [6.6 In-Game features](#66-in-game-features)
- [7. Feature not to be tested](#7-feature-not-to-be-tested)
- [8. Project Information](#8-project-information)

## **1. Test Objective**

### **1.1 Global resume**

Below are the essential features that must be available for beta testing.

| **Feature Name**   | **Description**                                                                                 | **Priority (High/Medium/Low)** |
|--------------------|-------------------------------------------------------------------------------------------------|--------------------------------|
| Multiplayer        | Enable multiple players to join the same session, with synchronized movement, interaction, and basic co-op functionality. | High                           |
| AI Expansion     | Upgrad e AI logic to create more dynamic and reactive behaviors. This includes: <br> - **Navigation & Pathfinding:** Smarter movement through complex environments, avoiding obstacles and using cover. <br> - **Combat Behavior:** Enemies adapt to player tactics, flank, retreat when damaged, and coordinate in groups. <br> - **Environmental Interaction:** AI can manipulate certain objects (e.g., opening doors, triggering traps, or altering light sources). <br> - **Perception System:** Improved detection using sight, sound, and environmental cues for more immersive stealth and combat encounters. <br> - **HUD Pixelization Feedback:** When AI interferes with systems, the HUD partially pixelates, simulating environmental distortion and player disorientation. | High |                          |
| New Weapons        | Introduce a wider range of firearms and tools, each with unique mechanics (e.g., damage types, reload systems, or utility functions). | High                           |
| Enemy Variety      | Add new enemy types with distinct attack patterns, abilities, and behaviors to diversify combat encounters. | Medium                         |
| Missions           | Expand mission content with tutorials, story-driven objectives, and exploration-focused tasks to guide player progression. | Medium                         |

---

### **1.2 Scope of testing**

The beta testing scope will focus on core gameplay validation and system stability. Specifically:

- Platform & Environment

    - PC with Windows OS
    - Distributed via Steam
    - Multiplayer support for 2–4 players

- Core Features
    - Multiplayer session creation, joining, and synchronization
    - AI navigation, combat behavior, and perception improvements
    - Weapon handling, reload mechanics, and utility variations
    - Interaction with new enemy types and mission objectives

- Non-Included Features (Out of Scope for Beta)
    - Full campaign storyline beyond Mission 2
    - Endgame content (advanced missions, bosses)
    - Advanced performance optimization and polish
    - Cosmetic systems (skins, customization)

---

### **1.3 Overview**

The beta version will include:

- Playable introduction sequence
- Complete Mission 1 with all objectives
- Partial Mission 2 to demonstrate exploration mechanics
- At least one different weapon
- One fully implemented Réplicant enemy type
- Core Fog mechanics with visual and gameplay effects
- Basic UI elements including health and objective tracking

---

## **2. Assumptions/constraints**

### **2.1 Assumptions**

- Testers will have access to a built version of the game
- Testers will have stable internet connections to support multiplayer sessions
- A limited ammount of content will be playable
- Testers are expected to provide structured feedback through designated channels (bug tracker, feedback forms, or communication platform).

### **2.2 Constraints**

- Some minor bugs might occur during testing due to compilation errors
- Multiplayer synchronization might not be precise, as the server used is public
- The game might have some performance issue depending on the configuration
- AI behaviors and mission objectives may not reflect final design balance or polish.

---

## **3. Known Issues & Limitations**

| **Issue** | **Description** | **Impact** | **Planned Fix? (Yes/No)** |
|----------|---------------|----------|----------------|
| Loading Times | Loading between areas may be longer than desired | Medium | Yes |
| Combat Balance | Weapon effectiveness against enemies may need adjustment | Medium | Yes |
| Fog Visual Effects | Some Fog effects may not be optimized for all hardware | Medium | Yes |

---

## **4. Software requierement**

### Minimum
- **Requires a 64-bit processor and operating system**
- **OS:** Windows 10  
- **Processor:** Intel Core i7-8700K / AMD Ryzen 5 1600X  
- **Memory:** 8 GB RAM  
- **Graphics:** NVIDIA GeForce GTX 1060 6 GB / AMD Radeon RX 5600 XT 6 GB / Intel Arc A380 6 GB  
- **DirectX:** Version 12  
- **Storage:** 55 GB available space  
- **Additional Notes:** SSD required. Minimum specs allow gameplay at 1080p 30FPS with Low settings.  

### Recommended
- **Requires a 64-bit processor and operating system**  
- **OS:** Windows 11  
- **Processor:** Intel Core i7-12700K / AMD Ryzen 7 5800X  
- **Memory:** 16 GB RAM  
- **Graphics:** NVIDIA GeForce RTX 3060 Ti 8 GB / AMD Radeon RX 6800 XT 16 GB  
- **DirectX:** Version 12  
- **Storage:** 55 GB available space  
- **Additional Notes:** SSD required. Recommended specs allow gameplay at 1080p 60FPS with High settings.  


---

## **5. Environmental Needs**

Global needs:
- Computer with requirements (see above)

Multiplayer:
- Steam with an account on computer
- 2-4 players

---

## **6. Test scenarios**

### **6.1 Main Menu**

#### **6.1.1 Create Lobby Button**

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Create lobby button |
| Objective | Create a multiplayer lobby as the host |
| Prerequisites | Game launched, in the main menu |
| Steps | A Create Lobby button is visible on the main menu. When pressed, it opens a lobby creation interface. The player can configure basic settings (e.g., lobby name, visibility, max players). Pressing Confirm creates a lobby and the player is placed inside it as the host. |

#### **6.1.2 Join Lobby Button**

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Join lobby button |
| Objective | Join an existing multiplayer lobby |
| Prerequisites | Game launched, in the main menu, another player is hosting a lobby |
| Steps | When pressing the button, a list of available lobbies is displayed. The player can select a lobby and join it successfully. If a lobby is full or no longer available, an error message is displayed. |

#### **6.1.3 Tutorial Button**

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Tutorial button |
| Objective | Start the tutorial |
| Prerequisites | Game launched, in the main menu |
| Steps | When pressed, it starts the tutorial sequence The player is placed into the tutorial environment. The tutorial can be exited back to the main menu at any time. |

#### **6.1.4 Settings Button**

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Settings button |
| Objective | Access the settings menu |
| Prerequisites | Game launched, in the main menu |
| Steps |When pressed, it opens the options menu with categories (Video, Audio, Keybinds). The player can change settings and confirm changes. The player can return to the main menu from the options menu. |

#### **6.1.5 Quit Game Button**

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Quit Game button |
| Objective | Quit the game |
| Prerequisites | Game launched, in the main menu |
| Steps | When pressed, it asks the player to confirm quitting. Confirming closes the game application Cancelling returns the player to the main menu. |

### **6.2 Tutorial Level**

#### **6.2.1 Tutorial Structure**

| **Section** | **Description** |
|-------------|----------------|
| Introduction | Basic movement controls (ZQSD), Sprint (Shift), Crouch (Ctrl), Jump (Space) |
| Combat Training | Weapon handling, reloading mechanics, melee combat with the pipe |
| Mini-games | Introduction to the 3 main mini-games used throughout missions |
| Fog Mechanics | Safe zones, fog effects, survival tactics |

#### **6.2.2 Mini-Games Details**

| **Mini-Game** | **Description** | **Controls** | **Success Criteria** |
|---------------|----------------|---------------|---------------------|
| Generator Repair | Match color sequences within time limit | Mouse clicks, E to interact | Complete sequence before timer expires |
| Door Hacking | Press buttons in correct order shown | Number keys (1-9) | Input correct code sequence |
| System Override | Hold position while defending against AI | ZQSD movement, mouse aim | Survive for required duration |

#### **6.2.3 Learning Objectives**

| **Skill** | **Practice Method** |
|-----------|-------------------|
| Movement | Obstacle course with jumping, crouching sections |
| Combat | Target practice area with both firearms and melee |
| Stealth | Avoid AI patrols in controlled environment |
| Mini-games | Practice area for each mini-game type |
| Team Coordination | Simple cooperative tasks requiring 2+ players |

#### **6.2.4 Tutorial Flow**

1. **Safe Room Start**
    - Basic movement controls
    - UI familiarization
    - Weapon selection

2. **Training Area**
    - Combat practice zone
    - Mini-game stations
    - AI behavior demonstration

3. **Practice Mission**
    - Small-scale mission combining all learned elements
    - Safe environment to test mechanics
    - Team coordination exercises

4. **Final Test**
    - Complete all mini-games under time pressure
    - Navigate fog-filled area
    - Defeat practice AI enemies
