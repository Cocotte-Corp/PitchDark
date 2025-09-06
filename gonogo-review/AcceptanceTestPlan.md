# **ACCEPTANCE TEST PLAN – PITCH DARK**

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

### **6.2 Settings Menu**

#### **6.2.1 Visual parameters**

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Visual parameters |
| Objective | Change visual settings |
| Prerequisites | Whether in main menu or in-game, Settings menu open |
| Steps | The player can open the Options → Video menu. The player can change resolution and graphics quality settings. Changes are applied immediately or after confirmation. Settings are saved and remain active after restarting the game. |

#### **6.2.1 Audio parameters**

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Audio parameters |
| Objective | Change audio settings |
| Prerequisites | Whether in main menu or in-game, Settings menu open |
| Steps | The player can open the Options → Audio menu. The player can adjust master volume, music volume, and sound effects volume. Changes are applied in real-time. Settings are saved and remain active after restarting the game. |

#### **6.2.3 Keybind parameters**

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Keybind parameters |
| Objective | Change Keybinds |
| Prerequisites | Whether in main menu or in-game, Settings menu open |
| Steps | The player can open the Options → Keybinds menu. The player can rebind movement keys, actions, and other Keybinds. The player can restore defaults at any time. Settings are saved and remain active after restarting the game. |

#### **6.3 Lobby**

#### **6.3.1 Player list**

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Player list |
| Objective | Get players info and status on lobby |
| Prerequisites | In a lobby with players |
| Steps | The lobby displays a list of all connected players. Each player’s username and profile picture are visible. The host is clearly identified in the list. Each player can toggle their Ready / Not Ready status. The current status is visible to all players in the lobby. The lobby prevents the game from starting until minimum requirements are met (e.g., minimum players, all players ready). |

#### **6.3.2 Host privileges**

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Keybind parameters |
| Objective | Start the game |
| Prerequisites | In a lobby with players, being the host |
| Steps | The host has the ability to start the game once all conditions are met. The host can see which players are ready and which are not. If a player disconnects or leaves, the lobby updates immediately. If the host leaves, host migration occurs (if supported) or the lobby closes. |

#### **6.3.3 All players privileges**

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | All players privileges |
| Objective | Various |
| Prerequisites | In a lobby with players |
| Steps | Players can leave the lobby at any time and return to the main menu. The lobby updates in real-time when players join, leave, or change status. Error handling is provided (e.g., if the host starts the game but a player disconnects at the same moment). |

### **6.4 Player behaviour**

#### **6.4.1 Player input**

| **Scenario** | **Description** |
|--------------|-----------------|
| **Functionality** | Movement Controls |
| **Objective** | Make the player move |
| **Prerequisites** | In a game |
| **Input list** |<ul> <li> **Move Forward** → Default: Z</li> <li> **Move Left** → Default: Q </li> <li> **Move Backward** → Default: S </li> <li> **Move Right** → Default: D </li><li>**Jump** → Default: Space</li><li>**Crouch** → Default: LeftCtrl</li><li>**Sprint** → Default: Maj (Shift)</li><li>**Interact with elements** → Default: E</li><li>**Shoot / Attack with weapon** → Default: Lmb (or equivalent)</li><li>**Change Weapon** → Default: 1, 2, 3</li>
| **General behaviour** | <ul><li> Movement responds immediately to input and stops when the key is released.</li><li>Diagonal movement is possible by combining keys (e.g., forward + left). </li><li>Can only jump while on the ground.</li><li>Can only sprint while moving forward.</li><li>Controls respond with minimal input latency.</li><li>Input conflicts are handled (e.g., pressing crouch + sprint).</li><li>The system provides feedback when an action cannot be performed (e.g., no ammo, blocked path).lt LeftClick)</li></ul>

#### **6.4.2 Feedback**

The game provides clear and responsive feedback in the following areas:


| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Button Interactions |
| Behaviour | <ul><li>Visual and/or audio cues are triggered when any buttonis hovered over, pressed, orreleased.</li><li>Disabled buttons arevisually distinct</li></ul>

---

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Player Actions |
| Behaviour | <ul><li>Immediate feedback is given for actions such as movement,jumping, shooting,interacting, or taking damage(e.g., sound effects, screenshake, UI indicators).</li><li>Health and status changes are clearly communicated viathe HUD.</li></ul>

---

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Quest Progression |
| Behaviour | <ul><li>Notifications or UI updates inform the player of quest objectives, progress, andcompletion.</li><li>Errors or failed objectives are clearly indicated</li></ul>

---

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Mini Games |
| Behaviour | <ul><li>Success, failure, and progress within mini gamesare communicated through visual and/or audio feedback..</li><li>Instructions and results are clearly displayed to the player.</li></ul>

#### **6.4.3 Weapons**

Each weapon has unique stats (damage, fire rate, range, reload speed).
Below is a list of available weapons:

| **Weapon** | **Description** |
|----------|---------------|
| Rifle | automatic fire, high damage, slower reload |
| Pistol | semi-automatic, faster reload, lower damage |
| Metal Pipe | melee weapon, unlimited use, no ammunition required |

---

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Ammunition |
| Objective | Loot ammunition |
| Prerequisites | In a game |
| Steps | Players can find and collect magazines for their firearms (rifle and pistol). Looted magazines are stored in the inventory system. Ammunition is consumed when firing and decreases from the inventory count. Magazines must match the weapon type (e.g., pistol magazines cannot be used in rifles). |

---

| **Scenario** | **Description** |
|----------|---------------|
| Functionnality | Reloading |
| Objective | Reloading the weapon |
| Prerequisites | In a game, weapon in hand |
| Steps | A weapon can only be reloaded if the player has at least one magazine in inventory. Reloading consumes one magazine and refills the weapon’s ammo clip. If no magazines are available, the reload action fails and a “No ammo” feedback is displayed. Reload animations and timing differ per weapon type (longer for rifle, shorter for pistol). |

---

- Players cannot shoot while running.
- Attempting to fire while sprinting provides feedback (e.g., click sound, UI indicator).
- Players must stop sprinting (stand still or walk) before firing.
- Melee attacks (metal pipe) can still be used while running.
- Weapon switching is instantaneous or delayed depending on design (swap animation).
- All actions (shooting, reloading, switching) include animations and sound feedback.
- The system prevents exploits such as infinite ammo, skipping reload, or shooting without delay.

### **6.5 AI Behaviour**

| **Scenario**  | **Description**                                                                                               |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Functionality | Enemy patrol                                                                                                  |
| Objective     | Make AI follow a predefined or random route                                                                   |
| Prerequisites | Enemy spawned in game world                                                                                   |
| Steps         | When idle, AI follows a patrol path. If the player is not detected, the AI continues patrolling according to parameters (loop, back and forth, stay). |

| **Scenario**  | **Description**                                                                                                                                      |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Functionality | Enemy vision                                                                                                                                         |
| Objective     | Detect player presence via line of sight                                                                                                             |
| Prerequisites | Player enters AI’s field of view                                                                                                                     |
| Steps         | If the player is visible within AI’s detection cone and range, AI becomes alerted and initiates pursuit. Obstacles can block detection. |

| **Scenario**  | **Description**                                                                                                |
| ------------- | -------------------------------------------------------------------------------------------------------------- |
| Functionality | Enemy hearing                                                                                                  |
| Objective     | Detect player presence through sound                                                                           |
| Prerequisites | Player produces noise (footsteps, gunfire, interaction) within AI’s hearing radius                             |
| Steps         | AI reacts to the sound by moving toward the source. If the player is confirmed visually or by contact, AI initiates pursuit. |

| **Scenario**  | **Description**                                                                                                                             |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| Functionality | Enemy chase                                                                                                                                 |
| Objective     | Make AI pursue detected players                                                                                                             |
| Prerequisites | Player detected through sight or hearing                                                                                                    |
| Steps         | AI increases movement speed, navigates obstacles, and follows the player. Chase continues until line of sight is broken for a set duration. |

| **Scenario**  | **Description**                                                                                            |
| ------------- | ---------------------------------------------------------------------------------------------------------- |
| Functionality | Enemy attack                                                                                               |
| Objective     | Damage the player when in range                                                                            |
| Prerequisites | Player in melee range of AI                                                                                |
| Steps         | AI performs attack animation and applies damage if successful. Cooldown prevents repeated instant attacks. |

| **Scenario**  | **Description**                                                                                      |
| ------------- | ---------------------------------------------------------------------------------------------------- |
| Functionality | Enemy opening doors                                                                                  |
| Objective     | Prevent safe zones behind closed doors                                                               |
| Prerequisites | AI chasing or patrolling, door in path                                                               |
| Steps         | AI interacts with door to open it. If locked, AI may attempt forced entry (depending on enemy type). |


| **Scenario**  | **Description**                                                                               |
| ------------- | --------------------------------------------------------------------------------------------- |
| Functionality | Enemy spawn                                                                                   |
| Objective     | Introduce enemies dynamically                                                                 |
| Prerequisites | Triggered event                                                                               |
| Steps         | AI spawns at designated or randomized points. Spawn can be immediate, timed, or event-driven. |

| **Scenario**  | **Description**                                                                                                                               |
| ------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Functionality | Enemy sounds                                                                                                                                  |
| Objective     | Add immersion and indirect feedback                                                                                                           |
| Prerequisites | Enemy active in game                                                                                                                          |
| Steps         | AI emits audio cues such as footsteps, growls, or screams. These can alert players and indicate enemy state (patrolling, alerted, attacking). |

| **Scenario**  | **Description**                                                                         |
| ------------- | --------------------------------------------------------------------------------------- |
| Functionality | Enemy jumpscare                                                                         |
| Objective     | Startle player through sudden scripted/dynamic event                                    |
| Prerequisites | Trigger zone or scripted event                                                          |
| Steps         | AI appears suddenly, with visual and/or audio cue. May transition into chase or attack. |

| **Scenario**  | **Description**                                                                                                         |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Functionality | Enemy death                                                                                                             |
| Objective     | Remove AI from gameplay upon defeat                                                                                     |
| Prerequisites | Enemy health reduced to zero                                                                                            |
| Steps         | AI plays death animation, emits sound, and despawns after a delay. Death may trigger item drops or mission progression. |

### **6.6 In-Game Multiplayer**

| Feature                | Description |
|-------------------------|-------------|
| **Player Visibility**  | - While alive, players can observe others’ actions (movement, shooting, interacting).<br> - Animations and actions are synchronized across clients (e.g., reloads are visible).<br> - Actions are updated in real time for immersion. |
| **Spectator Mode (Dead Players)** | - When dead, players enter Spectator Mode.<br> - Can watch teammates’ POVs.<br> - Supports manual switching or auto-follow.<br> - Updates in real time with active players’ movements and actions.<br> - Spectators cannot influence gameplay (no interaction, no unfair comms). |


---

## **7. Feature not to be tested**

- Character customization
- Room settings
- Sliding menu


---

## **8. Project Information**

- **Project Name:** Pitch Dark
- **Team Members:** Amaury Bariety, Bastien Rodrigues, Cyprien Nguyen-Van-Vien, Damien Benais-Captal and Viktor Bruggeman
- **Repository:** [Github](https://github.com/Cocotte-Corp/PitchDark)
