# Learning-unity
A collection of games I made by following the official courses "unity essentials" and "junior programming pathway" from unity

Playable WebGL Builds: All games are published and playable directly in your browser on Unity Play.
Link: https://play.unity.com/en/user/b1b08e8e-46eb-49a3-b5c4-8d726c9405f7

Unity Essentials: 
A multi-room interactive hub featuring scene selection navigation (Playground, Kid's Room 3D, Kitchen Audio, Living Room Programming, and Top-Down 2D)

Driving car game:
A 3D vehicle control project. Features forward movement, horizontal steering, obstacle placement, and smooth camera tracking behind the vehicle.

Plane Challenge 
Overview: A flight control game focusing on debugging reversed flight vectors, controlling plane pitch with user input, side-view camera tracking, and spinning propeller scripts.

Ball on Dome:
A physics-driven project centered around balance, transform manipulations, powerup pickup, and gravity physics on an elevated platform.

Feed the Animals: 
Overview: A top-down feeding mechanic featuring randomized animal spawning arrays (Instantiate), player movement bounds and projectile launching

Key challenges faced:

Missing Prefab References and Destroyed GameObjects

The Issue: Encountered a game-breaking MissingReferenceException when spawning animals in Prototype 2. The script attempted to access .transform.rotation on a destroyed or unassigned prefab in the array, causing input actions (like throwing food with the spacebar) to freeze entirely.

The Solution: Added null checks prior to instantiating and double-checked the Inspector array to make sure prefabs were assigned from the Project window rather than scene hierarchy instances.

Frame-Rate Independent Movement and Inverted Physics

The Issue: In the Plane and Vehicle projects, objects initially flew/drove wildly fast because movement was not frame-rate independent. In the plane challenge, movement vectors were also reversed, causing the plane to fly backward uncontrollably.

The Solution: Multiplied all translation and rotation inputs by Time.deltaTime and corrected the directional vectors (for example, changing Vector3.back to Vector3.forward).


What I learned overall:

3D navigation: Learned how to move, rotate and scale objects to create a scene

C# Scripting Fundamentals: Gained hands-on proficiency with object-oriented C# concepts including arrays, Instantiate(), Destroy(), InvokeRepeating(), vector math (Vector3), 

Physics and Collisions: Mastered key physics components in Unity, including Rigidbodies, Box Colliders, and the difference between physical collisions and trigger-based interactions (OnTriggerEnter).

Debugging and Problem Solving: Learned how to read Unity console errors, trace null references, fix camera tracking offsets, and systematically debug broken starter code.

Portfolio and Version Control: Built hands-on experience structuring Unity assets, using GitHub, and deploying WebGL projects to Unity Play.
