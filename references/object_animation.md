# 3D Object & Isometric Animation

## Isometric grid assembly
Individual isometric cubes/tiles should assemble with staggered entrance (each tile scales in from 0, ease-out-back, 40-80ms stagger), building the grid in a clear directional pattern (e.g. back-to-front or center-outward) rather than randomly.

## Product object rotation (phones, devices)
Rotation should be slow and purposeful — a 15-30° tilt/rotation over 2-3s, ease-in-out, often paired with a slight camera orbit in the same rotational direction for added dimensionality. Never spin a hero product object more than ~45° in a single shot — full rotations belong to explicit "360 product view" moments only.

## Floating/orbiting elements
Small decorative 3D elements (spheres, icons) orbiting a central object should move at consistent, slow angular velocity with a very slight vertical bob (sine-wave, small amplitude) to avoid feeling mechanically perfect.

## Node graphs / flowcharts
Nodes appear via scale-pop (ease-out-back), connector lines draw on via trim-path *after* both connected nodes have appeared (never before) — sequence: node A appears → node B appears → connecting line draws A to B. Branch/split points should have a brief anticipation pause before the split animates.

## Cloud/particle/glow elements
Ambient particles drift slowly and continuously (never a hard start/stop), with soft opacity fade at the edges of their motion range rather than appearing/disappearing abruptly. Individual particle motion should be non-uniform (varied speed/direction per particle) to avoid a mechanical look — call this "organic particle drift with varied timing" in prompts.

## Depth & light consistency
All 3D elements in a scene must share one light source direction and one perspective system — state this explicitly for any multi-object 3D scene: *"consistent top-left light source and isometric perspective across all elements."*
