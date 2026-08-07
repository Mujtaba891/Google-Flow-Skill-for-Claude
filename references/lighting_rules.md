# Lighting Rules

## Ambient lighting
Set an overall scene brightness/mood first, before any accent lighting: dark-mode scenes should stay genuinely dark (avoid the model brightening the whole frame to "see" the UI — specify *"scene remains dark, elements are lit by their own glow, not ambient light"*).

## Rim lighting
A thin bright edge-light on 3D objects/cards separates them from the background and adds premium polish. Prompt phrase: *"subtle rim light along the top edge of the card, separating it from the background."*

## Glow intensity
Glow should be motivated (a button, an accent color, a "hot" data point) — not applied uniformly across the frame. Specify intensity relative to the element's importance: hero elements get the strongest glow, secondary elements get 30-50% of that intensity.

## Bloom thresholds
Bloom (light bleeding beyond an element's edges) should trigger only on the brightest accent elements — if everything blooms, nothing reads as bright. Say *"bloom limited to the brightest highlight only"* to prevent over-application.

## Shadow softness
Soft, diffused shadows (large blur radius, low opacity, 15-25%) read as premium/modern. Hard-edged shadows read as dated/flat design — avoid unless deliberately going for a sharp/graphic-design aesthetic.

## Glass reflections
Glass/translucent UI panels should show a very subtle gradient reflection (a soft diagonal highlight band), not a literal mirror reflection — over-detailed reflections distract from content and can look glitchy in AI generation. Keep it minimal: *"subtle soft reflection highlight across the glass panel, not a literal mirror image."*

## Consistency across a sequence
Lock light source direction and color temperature across all scenes in a sequence unless a deliberate mood shift is part of the story (see `ui_animation.md`'s theme-transition pattern for the one common exception).
