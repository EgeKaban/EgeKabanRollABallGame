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
