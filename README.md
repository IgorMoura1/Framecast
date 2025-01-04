# Framecast 🎥
Landing page styled as a broadcast room with looping videos. Built using _**Three.js**_ and _**dat.GUI**_, it features a 3D grid of video planes. Videos serve as textures with dynamically calculated positions, rotations, and parallax effects. A camera and WebGL renderer display the scene, while mouse movement triggers animations, adding interactivity.

## Explaining the project 🛠️
Using the _**Three.js**_ library, where a grid of video planes is displayed. The data array contains objects with paths to various video files that will be used as textures on the planes. The params object holds various configuration settings for the grid, such as the number of rows and columns, spacing between planes, and curvature parameters.

A _**Three.js**_ scene is created using new THREE.Scene(), and a perspective camera is set up with a field of view of 25 degrees. The camera's position is set to (0, 0, 40) to provide a good view of the grid. A WebGL renderer is also created and configured to fill the entire window, with a white background color. The renderer's DOM element is appended to the document body to display the scene.

The code includes a debug mode controlled by the DEBUG_MODE variable. If enabled, a GUI is created using the dat.GUI library, allowing real-time adjustments to the parameters in the params object. This helps in fine-tuning the appearance and behavior of the grid.

Mouse movement is tracked to update the rotation and translation of a header element, creating a parallax effect. The createVideoElement function creates and configures a video element for each video source. The calculateRotations and calculatePosition functions compute the rotations and positions of the planes based on the grid configuration and curvature parameters.

The createVideoPlane function generates a plane with a video texture, using the calculated positions and rotations. Each plane's user data includes various properties for parallax and oscillation effects. The updateGallery function refreshes the grid by removing existing planes and creating new ones based on the current parameters.

The animate function is responsible for the animation loop, updating the header's transformation and the planes positions and rotations based on mouse movement and time. The camera is continuously adjusted to look at a target point, and the scene is rendered in each frame. The updateGallery and animate functions are called to initialize and start the animation.

## How execute the project ▶️

Make sure that node.js is install on your machine, if isn't go to Node.js download page and install [NodeJS](https://nodejs.org/en/download).

After that, navigate to your project directory and run the command in your terminal 
```
npm install http-server
```

Last but not least, run the command 
```
http-server
```
Then open the link provided in our terminal

### Enjoy the project 😁
