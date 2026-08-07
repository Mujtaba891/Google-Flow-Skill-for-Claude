# Composition Rules

## Rule of thirds
Place the hero element (headline, key card, focal metric) on a third-intersection, not dead center — dead-center compositions read as static/amateur. Exception: symmetrical "hero product shot" moments (e.g. a phone centered for a launch reveal) can break this deliberately.

## Negative space
Premium SaaS motion graphics are not busy. Aim for 40-60% empty/background space in any given frame even at the "fullest" moment of a scene. If a prompt is describing more than 4-5 distinct visual elements in one shot, split it into two shots.

## Balance & alignment
UI elements should align to an implied grid even when floating in 3D space — cards at consistent angles/depths, not randomly scattered. When prompting, say *"aligned to a consistent grid, floating at matched depth"* rather than leaving placement to chance.

## Focal point & eye flow
Every scene needs exactly one focal point at any given moment. Eye flow should move in one of: left-to-right (reading direction, most common), center-outward (radial reveal), or bottom-to-top (growth/upward momentum — good for metrics/growth content). State the intended eye flow explicitly for multi-element scenes.

## Grid systems
Isometric/3D scenes should imply an underlying grid (cube grids, card grids) even when the camera is moving — this is what makes `object_animation.md`'s isometric patterns read as intentional rather than chaotic.

## Layer depth
Minimum 3 depth layers for a scene with any camera movement: background (gradient/particles), midground (secondary UI/decorative elements), foreground (hero element). Each layer should have a distinct, slightly different motion speed (parallax) — background slowest, foreground matches camera speed most closely.
