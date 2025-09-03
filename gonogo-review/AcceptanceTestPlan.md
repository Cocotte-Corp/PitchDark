# **ACCEPTANCE TEST PLAN – PITCH DARK**

## **1. Core Functionalities for Beta Version**
Below are the essential features that must be available for beta testing.

| **Feature Name**  | **Description** | **Priority (High/Medium/Low)** |
|-------------------|---------------|--------------------------------|
| Player Movement & Interaction  | Basic movement controls and environment interaction capabilities | High |
| Fog (Pitch) Mechanic  | Progressive expansion and environmental alteration with pixelization of HUD | High |
| Combat System  | Functional weapons (firearms) with basic combat mechanics | High |
| Réplicant Enemies  | AI-driven enemies with scanning and mimicry abilities | Medium |
| Mission Structure  | Tutorial mission (Reactivating Primary Systems) and exploration mission (Locating Priority Repairs) | Medium |

---

## **2. Current expected features**

---

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

    Player is able to trigger the following inputs:
        - Move forward (default Z)
        - Move Left (default Q)
        - Move Backward (default S)
        - Move Right (default D)
        - Jump (default Space)
        - Crouch (Default LeftCtrl)
        - Interact with elements (default E)
        - Sprint (defa ult Maj)
        - Change weapon (default 1, 2, 3)
        - Shoot/Attack with weapon (default LeftClick)

#### **2.2.2 Animations**

#### **2.2.3 Weapons**

    Three differents weapons available:
        - Riffle gun
        - Pistol
        - Metal pipe

    Players can loot magazines for their weapons.
    Players are able to reload a weapon ONLY IF magazines in inventory.
    Players cannot shoot while running.

### **2.3 AI Behaviour**

### **2.4 Multiplayer functionalities**

---

## **3. Success Criteria**
The following criteria will be used to determine the success of the beta version.

| **Criterion** | **Description** | **Threshold for Success** |
|--------------|---------------|------------------------|
| Completion Rate | Players can complete Mission 1 without getting stuck | 80% of testers |
| Atmosphere | Players report the game atmosphere as "tense" or "scary" | 70% of testers |
| Mechanics Understanding | Players understand core mechanics after first mission | 75% of testers |
| Technical Performance | Frame rate maintains target performance | At least 30 FPS on target hardware |
| Bug Frequency | Game-breaking bugs are rare | Less than 10% of testers encounter any |
| Player Interest | Players express interest in the full game | 70% of testers |

---

## **4. Known Issues & Limitations**

| **Issue** | **Description** | **Impact** | **Planned Fix? (Yes/No)** |
|----------|---------------|----------|----------------|
| Loading Times | Loading between areas may be longer than desired | Medium | Yes |
| Combat Balance | Weapon effectiveness against enemies may need adjustment | Medium | Yes |
| Fog Visual Effects | Some Fog effects may not be optimized for all hardware | Medium | Yes |

---

## **5. Deliverables & Format**
The beta version will include:

- Playable introduction sequence
- Complete Mission 1 with all objectives
- Partial Mission 2 to demonstrate exploration mechanics
- At least one different weapon
- One fully implemented Réplicant enemy type
- Core Fog mechanics with visual and gameplay effects
- Basic UI elements including health and objective tracking

---

## **Project Information**

- **Project Name:** Pitch Dark
- **Team Members:** Amaury Bariety, Bastien Rodrigues, Cyprien Nguyen-Van-Vien, Damien Benais-Captal and Viktor Bruggeman
- **Repository:** [Github](https://github.com/Cocotte-Corp/PitchDark)
