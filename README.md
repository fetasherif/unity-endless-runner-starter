
Unity Beginner Endless Runner Template (V1)
Hey! Welcome to my little endless runner prototype built in Unity.

I put this together as a lightweight, clean boilerplate specifically for beginners trying to wrap their heads around how basic 3D movement, procedural spawning, and smooth camera controls work in Unity without getting bogged down by overly complex, bloated architecture.


Why I Built This 
Working on a lower-spec setup (my current machine is rocking a modest 4GB of RAM) forces you to be mindful of how you write code. You quickly learn to keep scripts modular, avoid unnecessary overhead, and focus on raw performance and logic rather than relying on heavy asset packs.

This V1 template is designed to be super lightweight and easy to drop into a blank project.


What's Inside (V1 Features)
•	Movement.cs: Handles lane-switching (supports both Arrow keys and A/D) with clean bounds clamping, progressive speed scaling that increases over time, and smooth horizontal interpolation. (Note: Left the Rigidbody out of the active motion loop for now to keep movement snappy and straightforward for learners).

•	ground_spawner.cs: A simple starter spawner that instantiates an initial sequence of ground tiles so you can immediately see the procedural logic in action.

•	camerafollowe.cs: Uses independent axis smoothing (SmoothDamp) to give the camera that nice, floating cinematic lag behind your player.

How to Use It
1.	Clone or download this repo into your Unity project (Unity 2022 LTS or newer recommended).

2.	Create a basic 3D object (like a cylinder) to act as your placeholder player. 

3.	Attach the Movement script and the camerafollowe script to your player. 

4.	Create an empty GameObject, attach ground_spawner, and plug in your ground tile prefab.

5.	Hit Play!

What’s Coming in V2?
Because V1 is meant to be a bare-bones learning tool, it has a few limitations (like spawning a fixed number of tiles at startup instead of an infinite recycling loop).

For V2, I'm planning to tackle:


•	Infinite Tile Recycling / Object Pooling: Reusing old ground chunks instead of letting them pile up in memory to keep things optimized.

•	Obstacle Spawning: Adding randomized hazards across the lanes.

•	Clean UI & Score Tracking: A simple start/game-over loop.

Feel free to fork it, break it, and learn from it. If you have any suggestions or cleaner ways to handle things, pull requests are always welcome!

