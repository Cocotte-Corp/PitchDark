# **ACCEPTANCE TEST PLAN – PITCH DARK**

## **1 Test Objective**

Below are the essential features that must be available for beta testing.

| **Feature Name**   | **Description**                                                                                 | **Priority (High/Medium/Low)** |
|--------------------|-------------------------------------------------------------------------------------------------|--------------------------------|
| Multiplayer        | Enable multiple players to join the same session, with synchronized movement, interaction, and basic co-op functionality. | High                           |
| AI Expansion     | Upgrad e AI logic to create more dynamic and reactive behaviors. This includes: <br> - **Navigation & Pathfinding:** Smarter movement through complex environments, avoiding obstacles and using cover. <br> - **Combat Behavior:** Enemies adapt to player tactics, flank, retreat when damaged, and coordinate in groups. <br> - **Environmental Interaction:** AI can manipulate certain objects (e.g., opening doors, triggering traps, or altering light sources). <br> - **Perception System:** Improved detection using sight, sound, and environmental cues for more immersive stealth and combat encounters. <br> - **HUD Pixelization Feedback:** When AI interferes with systems, the HUD partially pixelates, simulating environmental distortion and player disorientation. | High |                          |
| New Weapons        | Introduce a wider range of firearms and tools, each with unique mechanics (e.g., damage types, reload systems, or utility functions). | High                           |
| Enemy Variety      | Add new enemy types with distinct attack patterns, abilities, and behaviors to diversify combat encounters. | Medium                         |
| Missions           | Expand mission content with tutorials, story-driven objectives, and exploration-focused tasks to guide player progression. | Medium                         |

---

## **1.2 Scope of testing**

/*to be done*/

---

## **1.3 Overview**

The beta version will include:

- Playable introduction sequence
- Complete Mission 1 with all objectives
- Partial Mission 2 to demonstrate exploration mechanics
- At least one different weapon
- One fully implemented Réplicant enemy type
- Core Fog mechanics with visual and gameplay effects
- Basic UI elements including health and objective tracking

---

## **Assumptions/constraints**

/*to be done*/

---

## **4. Known Issues & Limitations**

| **Issue** | **Description** | **Impact** | **Planned Fix? (Yes/No)** |
|----------|---------------|----------|----------------|
| Loading Times | Loading between areas may be longer than desired | Medium | Yes |
| Combat Balance | Weapon effectiveness against enemies may need adjustment | Medium | Yes |
| Fog Visual Effects | Some Fog effects may not be optimized for all hardware | Medium | Yes |

---

## **Software requierement**

## System Requirements

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

## **Environlental Needs**

/*to be done*/

---

## **Testing procedure**

### **2.1 Main menu**

    Create Lobby Button:
        A Create Lobby button is visible on the main menu.
        When pressed, it opens a lobby creation interface.
        The player can configure basic settings (e.g., lobby name, visibility, max players).
        Pressing Confirm creates a lobby and the player is placed inside it as the host.

    Join Lobby Button:
        A Join Lobby button is visible on the main menu.
        When pressed, it displays a list of available lobbies.
        The player can select a lobby and join it successfully.
        If a lobby is full or no longer available, an error message is displayed.

    Tutorial Button:
        A Tutorial button is visible on the main menu.
        When pressed, it starts the tutorial sequence.
        The player is placed into the tutorial environment.
        The tutorial can be exited back to the main menu at any time.

    Options Button:
        An Options button is visible on the main menu.
        When pressed, it opens the options menu with categories (Video, Audio, Keybinds).
        The player can change settings and confirm changes.
        The player can return to the main menu from the options menu.

    Quit Game Button:
        A Quit button is visible on the main menu.
        When pressed, it asks the player to confirm quitting.
        Confirming closes the game application.
        Cancelling returns the player to the main menu.

#### **2.1.1 Settings**

    Visual Parameters:
        The player can open the Options → Video menu.
        The player can change resolution and graphics quality settings.
        Changes are applied immediately or after confirmation.
        Settings are saved and remain active after restarting the game.

    Audio Parameters:
        The player can open the Options → Audio menu.
        The player can adjust master volume, music volume, and sound effects volume.
        Changes are applied in real-time.
        Settings are saved and remain active after restarting the game.

    Key Bindings:
        The player can open the Options → Keybinds menu.
        The player can rebind movement keys, actions, and other Keybinds.
        The player can restore defaults at any time.
        Settings are saved and remain active after restarting the game.

#### **2.1.2 Lobby**

    Player List:
        The lobby displays a list of all connected players.
        Each player’s username and profile picture are visible.
        The host is clearly identified in the list.
        Ready Status
        Each player can toggle their Ready / Not Ready status.
        The current status is visible to all players in the lobby.
        The lobby prevents the game from starting until minimum requirements are met (e.g., minimum players, all players ready).

    Host Controls:
        The host has the ability to start the game once all conditions are met.
        The host can see which players are ready and which are not.
        If a player disconnects or leaves, the lobby updates immediately.
        If the host leaves, host migration occurs (if supported) or the lobby closes.

    General Behavior:
        Players can leave the lobby at any time and return to the main menu.
        The lobby updates in real-time when players join, leave, or change status.
        Error handling is provided (e.g., if the host starts the game but a player disconnects at the same moment).

### **2.2 Player behaviour**

#### **2.2.1 Player input**

    Movement Controls:
        Move Forward → Default: Z
        Move Left → Default: Q
        Move Backward → Default: S
        Move Right → Default: D
        Movement responds immediately to input and stops when the key is released.
        Diagonal movement is possible by combining keys (e.g., forward + left).
        Traversal Controls
        Jump → Default: Space
        Triggers the jump animation and vertical movement.
        Jump is only possible when on the ground.
        Crouch → Default: LeftCtrl
        Reduces player height and movement speed.
        Used to access low areas or stealth gameplay.
        Toggles or hold behavior depending on options.
        Sprint → Default: Maj (Shift)
        Increases movement speed while held.
        Disables shooting during sprinting (see weapons system).
        Interaction Controls
        Interact with elements → Default: E
        Allows picking up items, opening doors, pressing buttons, etc.
        Interaction is context-sensitive and works only when near an interactable element.

    Combat Controls:
        Shoot / Attack with weapon → Default: Left Mouse Button (or equivalent)
        Fire the equipped ranged weapon (if ammo is available).
        Swing or strike with melee weapon if equipped.
        Triggered action is blocked if conditions are not met (e.g., sprinting, no ammo).
        Change Weapon → Default: 1, 2, 3
        Instantly or gradually switches between available weapons (rifle, pistol, metal pipe).
        Feedback (UI + animation) confirms the weapon swap.

    General Requirements:
        All inputs must be rebindable in the Options → Controls menu.
        Controls respond with minimal input latency.
        Input conflicts are handled gracefully (e.g., pressing crouch + sprint).
        The system provides feedback when an action cannot be performed (e.g., no ammo, blocked path).lt LeftClick)

#### **2.2.2 Feedback**

    The game provides clear and responsive feedback in the following areas:
        - Button Interactions:
            - Visual and/or audio cues are triggered when any button is hovered over, pressed, or released.
            - Disabled buttons are visually distinct.
        - Player Actions:
            - Immediate feedback is given for actions such as movement, jumping, shooting, interacting, or taking damage (e.g., sound effects, screen shake, UI indicators).
            - Health and status changes are clearly communicated via the HUD.
        - Quest Progression:
            - Notifications or UI updates inform the player of quest objectives, progress, and completion.
            - Errors or failed objectives are clearly indicated.
        - Mini Games:
            - Success, failure, and progress within mini games are communicated through visual and/or audio feedback.
            - Instructions and results are clearly displayed to the player.

#### **2.2.3 Weapons**

    Available Weapons:
        Players have access to three weapon types:
        Rifle (automatic fire, high damage, slower reload).
        Pistol (semi-automatic, faster reload, lower damage).
        Metal Pipe (melee weapon, unlimited use, no ammunition required).
        Each weapon has unique stats (damage, fire rate, range, reload speed).
        Weapons can be swapped in-game depending on availability and inventory.

    Looting Ammunition:
        Players can find and collect magazines for their firearms (rifle and pistol).
        Looted magazines are stored in the inventory system.
        Ammunition is consumed when firing and decreases from the inventory count.
        Magazines must match the weapon type (e.g., pistol magazines cannot be used in rifles).

    Reloading:
        A weapon can only be reloaded if the player has at least one magazine in inventory.
        Reloading consumes one magazine and refills the weapon’s ammo clip.
        If no magazines are available, the reload action fails and a “No ammo” feedback is displayed.
        Reload animations and timing differ per weapon type (longer for rifle, shorter for pistol).

    Shooting Restrictions:
        Players cannot shoot while running.
        Attempting to fire while sprinting provides feedback (e.g., click sound, UI indicator).
        Players must stop sprinting (stand still or walk) before firing.
        Melee attacks (metal pipe) can still be used while running.

    General Behavior:
        Weapon switching is instantaneous or delayed depending on design (swap animation).
        All actions (shooting, reloading, switching) include animations and sound feedback.
        The system prevents exploits such as infinite ammo, skipping reload, or shooting without delay.

### **2.3 AI Behaviour**

### **2.4 Multiplayer functionalities**

### **2.4.1 Lobby functionalities**

    Create a Lobby:
        A player can select “Create Lobby” from the menu.
        The system generates a new lobby instance with configurable parameters (name, max players, visibility).
        The player who created the lobby is automatically assigned as the host.
        Destroy a Lobby
        The host can close/destroy the lobby at any time.
        If destroyed, all connected players are returned to the main menu with a message explaining the lobby was closed.
        If supported, host migration occurs (another player becomes the host).

    Join a Lobby:
        Players can browse a list of available lobbies.
        Players can join a selected lobby if it is open and not full.
        If the lobby is full or closed, a notification is displayed.
        Leave a Lobby
        Any player (host or guest) can leave the lobby at any time.
        Leaving redirects the player back to the main menu.
        If the host leaves, the lobby is either destroyed or migrated depending on design choice.

    Lobby Chat:
        Players inside the lobby can send text messages.
        Messages are visible in real-time to all other connected players.
        Each message is tagged with the sender’s username.
        Offensive or disruptive messages can be managed with a filter or moderation system (optional).

    Game Launch:
        Each player can toggle their Ready/Not Ready status.
        The host sees the status of all players.
        The game can only be launched when:
        The minimum player count is reached.
        All players are marked as Ready.
        Once started, all players are transitioned from the lobby to the game session simultaneously.

### **2.4.2 In-Game features**

    Player Visibility:
        While alive, players can observe the behaviors and actions of other players (e.g., movement, shooting, interacting).
        Animations and actions are synchronized across clients to ensure consistency (e.g., when a player reloads, others see it).
        The system ensures that visible actions are accurate and updated in real-time to maintain immersion.

    Spectator Mode (Dead Players):
        When a player dies, they enter Spectator Mode.
        In this mode, the dead player can watch other players’ points of view.
        The system cycles through perspectives of alive teammates (manual switch or auto-follow).
        The spectator view updates in real time with the active player’s movements, aiming, and actions.
        Spectators cannot influence gameplay (no interaction, no communication that provides unfair advantage).

---

## **Feature not to be tested**

/*to be done*/

---

## **Project Information**

- **Project Name:** Pitch Dark
- **Team Members:** Amaury Bariety, Bastien Rodrigues, Cyprien Nguyen-Van-Vien, Damien Benais-Captal and Viktor Bruggeman
- **Repository:** [Github](https://github.com/Cocotte-Corp/PitchDark)
