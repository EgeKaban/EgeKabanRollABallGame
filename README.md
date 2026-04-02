# EgeKabanRollABallGame

## Project Overview
This repository contains my implementation of the classic Unity **Roll-a-Ball** tutorial. This project serves as a midterm assignment to demonstrate fundamental Unity skills, including physics, user input, camera movement, object collection, and version control using GitHub.

**Unity Version:** 6.38f1

---

## Development Diary & Steps Completed

As per the assignment requirements, I successfully implemented the following core stages of the game:

1. **Setting up the game:** Created the base Unity project, set up the initial scene, and organized my file structure (Folders: `Scripts`, `Scenes`, `Materials`, `Prefabs`).
2. **Moving the player:** Added a Sphere to act as the player, attached a `Rigidbody` component for physics, and created a `PlayerController` script utilizing Unity's Input System to apply forces for movement.
3. **Moving the camera:** Wrote a `CameraController` script to calculate the offset between the camera and the player, allowing the camera to smoothly follow the ball without rotating with it.
4. **Setting up the play area:** Constructed the ground and surrounding walls to keep the player from falling off the edge. Applied custom materials to distinguish the ground from the walls.
5. **Creating collectibles:** Created cube objects, made them spin using a `Rotator` script, turned them into Prefabs, and scattered them across the play area. Implemented `OnTriggerEnter` in the player script to "collect" (deactivate) them upon collision.

---

## What I Learned
Through this project, I gained hands-on experience with several core game development concepts:
* **Physics & Rigidbodies:** Understanding how to move objects using physics forces rather than directly changing their transform positions.
* **Input System:** Capturing keyboard/controller inputs to control a game object.
* **Scripting Basics:** Using variables, `Update()`, `FixedUpdate()`, and `LateUpdate()` appropriately in C#.
* **Triggers vs. Colliders:** Learning the difference between hard collisions and trigger events (for the collectibles).
* **Version Control:** Setting up a `.gitignore` file specifically for Unity to prevent uploading massive `Library` and temporary files to GitHub.

---

## Challenges, Errors, & Solutions

*(Note: Below are examples. Edit these to match the actual errors you faced!)*

### 1. The Player Object Wouldn't Move
* **The Error:** Initially, when I pressed the arrow keys, the ball didn't move at all, even though there were no console errors.
* **The Fix:** I realized I forgot to attach the `PlayerController` script to the Player object in the Unity Inspector. Once attached and the `Rigidbody` was assigned, it worked perfectly.

### 2. Camera Rotating Wildly
* **The Error:** I accidentally made the Main Camera a child of the Player Sphere. When the ball rolled, the camera rolled with it, creating a dizzying effect.
* **The Fix:** I moved the camera out of the Player object in the hierarchy and created the `CameraController` script to maintain a steady offset using `LateUpdate()`.
* **AI Assistance Used:** > **Prompt:** "My Unity camera is spinning wildly when attached to my rolling ball player. How do I make it follow the ball without spinning?"
  > **AI Suggestion:** The AI explained the concept of `LateUpdate` and provided the basic math for maintaining a position offset without inheriting rotation.

### 3. GitHub Upload Issues
* **The Error:** My first commit was taking forever, and I realized I was trying to upload the `Library` folder.
* **The Fix:** I deleted the repository, created a new one, and made sure to generate a standard Unity `.gitignore` file before making my first commit. 

---

## BONUS: Custom Assets & Polish
*(Delete this section if you didn't do the bonus, or edit it if you did!)*

To make the game my own, I added some custom visual elements:
* **Custom Materials:** Changed the default colors of the ground, player, and collectibles.
* **Lighting:** Adjusted the directional light to create better shadows.
