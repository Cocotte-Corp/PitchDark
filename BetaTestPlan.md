# Beta Test Plan for Pitch Dark

## Sumary

- [Project Information](#project-information)
- [1. Selection of Core Functionalities](#1-selection-of-core-functionalities)
- [2. Definition of Beta Testing Scenarios](#2-definition-of-beta-testing-scenarios)
- [3. Coverage of Key User Journeys](#3-coverage-of-key-user-journeys)
- [4. Clear Evaluation Criteria](#4-clear-evaluation-criteria)
- [5. Deliverables & Format](#5-deliverables--format)

## Project Information

- **Project Name: Pitch Dark**
- **Team Members: Amaury Bariety, Bastien Rodrigues, Cyprien Nguyen-Van-Vien, Damien Benais-Captal and Viktor Bruggeman**
- **Repository: [Github](https://github.com/Cocotte-Corp/PitchDark)**

## 1. Selection of Core Functionalities

Based on the Pitch Dark concept document, I've identified the following core functionalities that must be available in the beta version:

### Core Gameplay Mechanics

- Player movement and basic interaction with the environment
- The Fog (Pitch) mechanic with progressive expansion and environmental alteration
- Basic combat system with functional weapons (both firearms and melee)
- Weapon degradation and enrayement (jamming) mechanics
- Mental health/sanity system affected by exposure to the Fog

### Essential Mission Structure

- Mission 1: Reactivating Primary Systems - This will serve as the tutorial mission
- Mission 2: Locating Priority Repairs - This will demonstrate exploration mechanics
- At least one encounter with a Réplicant enemy

## 2. Definition of Beta Testing Scenarios

### Scenario 1: Basic Navigation and Environment Interaction

**User Role:** Player (Robot character) Feature Being Tested: Movement and interaction with the environment Expected Outcome: Player can move freely through accessible areas and interact with key objects Steps to Execute:

- Start a new game and complete initial awakening sequence
- Navigate through the first corridor section
- Interact with doors, panels, and objects
- Test crouching, running, and other movement options
- Verify collision detection works properly with environment

### Scenario 2: The Fog (Pitch) Mechanic

**User Role:** Player Feature Being Tested: Fog expansion and effects Expected Outcome: The Fog visibly affects the environment and player perception Steps to Execute:

- Enter an area where the Fog is present
- Observe visual and audio distortion effects
- Remain in the Fog for 60 seconds and note mental health degradation
- Test using protective equipment to mitigate Fog effects
- Verify that the Fog expands over time as described in the design document

### Scenario 3: Combat System

**User Role:** Player Feature Being Tested: Weapon functionality and enemy interaction Expected Outcome: Weapons function as designed with appropriate feedback and damage Steps to Execute:

- Acquire both a firearm (pistol) and melee weapon (knife)
- Encounter a basic enemy
- Test firearm combat including aiming, firing, and reloading
- Test melee combat including different attack types
- Verify weapon degradation occurs with repeated use
- Test weapon jamming mechanics with firearms

### Scenario 4: Réplicant Enemy Encounter

**User Role:** Player Feature Being Tested: Réplicant AI and mimicry abilities Expected Outcome: Réplicant demonstrates scanning, mimicry, and adaptive behavior Steps to Execute:

- Trigger a Réplicant encounter
- Observe the Réplicant scanning behavior
- Test how the Réplicant responds to different player actions
- Verify that the Réplicant can mimic appearance and voice
- Test combat against the Réplicant to ensure proper difficulty balance

### Scenario 5: Mission 1 Completion

**User Role:** Player Feature Being Tested: Mission structure and objective tracking Expected Outcome: Player can complete all objectives with proper guidance and feedback Steps to Execute:

- Receive Mission 1 objectives
- Locate auxiliary power generators
- Repair damaged cables affected by the Pitch
- Avoid Réplicants attempting to sabotage efforts
- Access the main control room
- Reactivate life support systems
- Verify mission completion and reward

## 3. Coverage of Key User Journeys

### Primary User Journey: First Hour of Gameplay

- Player awakens from stasis and learns basic controls
- Player discovers the damaged state of the ship
- Player encounters the Fog for the first time
- Player acquires first weapons and encounters enemies
- Player receives Mission 1 objectives
- Player completes first mission objectives while managing resources
- Player experiences first major Réplicant encounter

### Edge Cases and Failure Points

- Player death and respawn mechanics
- Running out of ammunition during combat
- Weapon breaking during critical encounters
- Extreme mental health degradation from Fog exposure
- Getting trapped in areas being consumed by the Fog

## 4. Clear Evaluation Criteria

### Performance Metrics

- Frame rate must maintain at least 30 FPS on target hardware
- Loading times between areas should not exceed 15 seconds
- Combat responsiveness should have less than 100ms input lag

### Gameplay Metrics

- Players should be able to complete Mission 1 within 45-60 minutes
- First-time players should be able to understand core mechanics without excessive tutorial prompts
- Weapon degradation should be balanced to encourage strategic use without frustration
- Fog effects should create tension without being overly punishing in early gameplay

### Success Criteria

- 80% of testers can complete Mission 1 without getting stuck
- 70% of testers report the atmosphere as "tense" or "scary"
- 75% of testers understand the core mechanics after the first mission
- Less than 10% of testers encounter any game-breaking bugs
- 70% of testers express interest in playing the full game

## 5. Deliverables & Format

The beta version will include:

- Playable introduction sequence
- Complete Mission 1 with all objectives
- Partial Mission 2 to demonstrate exploration mechanics
- At least 3 different weapon types (1 firearm, 2 melee)
- One fully implemented Réplicant enemy type
- Core Fog mechanics with visual and gameplay effects
- Basic UI elements including health, mental state, and objective tracking
