# Prompt
Create a single HTML file that uses Matter.js to simulate falling letters inside a spinning container. The specifications are:
	1.	Canvas and Physics Setup:
	•	The page should use a full-screen HTML canvas with a dark (black) background.
	•	Use Matter.js (loaded via a CDN) to simulate physics with gravity.
	•	Ensure the canvas resizes with the window.
	2.	Spinning Container (Cube):
	•	Create a square container (a ‘cube’) with white walls that confines the letters. The container should have a configurable side length (e.g., 600 pixels) and wall thickness (e.g., 20 pixels).
	•	The container is composed of four static Matter.js bodies (top, bottom, left, right) that form its boundaries.
	•	The container should continuously spin (rotate) around its center. Update the positions and angles of the container walls each frame according to the current rotation.
	•	All falling letters must remain inside the container; they should bounce off its walls.
	3.	Falling Letters:
	•	Letters are spawned at a high rate (e.g., every 100 ms) within the container.
	•	Each letter is chosen randomly from A–Z, with a random font size between 30 and 80 pixels.
	•	Each letter is rendered as text using the canvas’s fillText (using a sans-serif font) in a randomly selected bright color (e.g., red, green, blue, yellow, magenta, cyan, or white).
	•	For physics, create a Matter.js rectangular body for each letter sized approximately to its font size. Give each letter a slight random initial angle (between –0.3 and 0.3 radians) so they fall and bounce dynamically.
	•	The letter bodies should spawn at random positions that are guaranteed to be inside the container. This may be done by generating positions in the container’s local coordinate system and transforming them to world coordinates based on the container’s current rotation.
	4.	Animation and Rendering:
	•	Update the physics engine at approximately 60 fps.
	•	In each render loop, update the container’s rotation, recalculate the positions of its walls, and then draw all bodies:
	•	Render letters using fillText (with proper translation and rotation according to their physics body positions and angles).
	•	Render the container walls as filled white polygons.
	•	Ensure no debug markers (like a red dot) are drawn.

The final output should be a self-contained HTML file with embedded JavaScript that fulfills the above requirements and works when served from a local or hosted server (e.g., GitHub Pages).