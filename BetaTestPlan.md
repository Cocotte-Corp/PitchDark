# **BETA TEST PLAN – PITCH DARK**

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

## **2. Beta Testing Scenarios**

### **2.1 User Roles**
The following roles will be involved in beta testing.

| **Role Name**  | **Description** |
|---------------|---------------|
| Player        | User controlling the Robot character, testing all gameplay features |

---

### **2.2 Test Scenarios**
For each core functionality, detailed test scenarios are provided below.

#### **Scenario 1: Basic Navigation and Environment Interaction**
- **Role Involved:** Player
- **Objective:** Ensure player can move freely and interact with the environment
- **Preconditions:** New game started
- **Test Steps:**
  1. Complete initial awakening sequence
  2. Navigate through the first corridor section
  3. Interact with doors, panels, and objects
  4. Test crouching, running, and other movement options
  5. Verify collision detection works properly with environment
- **Expected Outcome:** Player can move freely through accessible areas and interact with key objects

#### **Scenario 2: The Fog (Pitch) Mechanic**
- **Role Involved:** Player
- **Objective:** Verify Fog visual effects and gameplay impact
- **Preconditions:** Player has reached an area where Fog is present
- **Test Steps:**
  1. Enter an area where the Fog is present
  2. Observe visual and audio distortion effects
  3. Remain in the Fog for 60 seconds and note mental health degradation
  4. Test using protective equipment to mitigate Fog effects
  5. Verify that the Fog expands over time as described in the design document
- **Expected Outcome:** The Fog visibly affects the environment and player perception

#### **Scenario 3: Combat System**
- **Role Involved:** Player
- **Objective:** Test weapon functionality and enemy interaction
- **Preconditions:** Player has acquired a weapon
- **Test Steps:**
  1. Acquire a firearm (pistol)
  2. Encounter a basic enemy
  3. Test firearm combat including aiming, firing, and reloading
- **Expected Outcome:** Weapons function as designed with appropriate feedback and damage

#### **Scenario 4: Réplicant Enemy Encounter**
- **Role Involved:** Player
- **Objective:** Test Réplicant AI and mimicry abilities
- **Preconditions:** Player has reached a point where Réplicants appear
- **Test Steps:**
  1. Trigger a Réplicant encounter
  2. Observe the Réplicant scanning behavior
  3. Test how the Réplicant responds to different player actions
  4. Verify that the Réplicant can mimic appearance and voice
  5. Test combat against the Réplicant to ensure proper difficulty balance
- **Expected Outcome:** Réplicant demonstrates scanning, mimicry, and adaptive behavior

#### **Scenario 5: Mission 1 Completion**
- **Role Involved:** Player
- **Objective:** Verify mission structure and objective tracking
- **Preconditions:** Player has started Mission 1
- **Test Steps:**
  1. Receive Mission 1 objectives
  2. Complete required tasks while avoiding Réplicants
  3. Verify mission completion and reward
- **Expected Outcome:** Player can complete all objectives with proper guidance and feedback

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
