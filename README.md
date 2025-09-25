# ForcePhys v3 (Self-contained)

**ForcePhys v3** is a lightweight 2D physics engine wrapper around Matter.js. This version is fully self-contained and does **not** require loading Matter.js from a CDN.

## Features

- Gravity, friction, bounciness, density per body
- Circles and rectangles (polygons supported)
- Keyboard controls and mouse drag
- Collision events
- Visual debug mode
- Fully self-contained (no external scripts needed)

## Usage

1. Include the script in your HTML:

```html
<script src="ForcePhys-v3.min.js"></script>
<canvas id="myCanvas" width="800" height="600"></canvas>
<script>
const world = new ForcePhys.World({ canvasId: 'myCanvas', gravity: 1 });

// Add objects
world.add(ForcePhys.Circle({ x:200, y:100, r:30, color:'red', id:'ball' }));
world.add(ForcePhys.Rect({ x:400, y:550, w:800, h:30, color:'blue', static:true }));

world.start();
</script>
