# Animation System (Property-Level Rules)

How to describe *what* is animating, precisely enough for a text-to-video model to render it consistently.

## Core properties and how to phrase them

- **Scale**: always pair with easing + origin point. *"scales up from 90% to 100% from its center, ease-out-back"*. Avoid bare "scales up."
- **Position**: describe start point, end point, and path shape. *"slides in from the right edge along a gentle upward arc, settling at center-left"*.
- **Rotation**: keep small for UI elements (2-8°) unless it's a deliberate 3D flip. *"tilts 4 degrees on the Y-axis as it enters, settling flat"*.
- **Morphing**: only between shapes with clear topological relationship (circle→blob, line→icon). Name both states explicitly: *"the loading dot morphs into a checkmark icon over 0.4s"*.
- **Shape layers / stroke animation**: for icons, logos, flowchart lines. *"the connector line draws on from left to right, stroke width 2px, rounded caps"*.
- **Trim paths**: for circular progress, icon reveals. *"the ring trims on clockwise from 0% to 100%, ending in a settle bounce"*.
- **Mask reveals**: for text and image reveals without literal movement. *"headline is revealed via a left-to-right wipe mask, edge is soft not hard"*.
- **Blur transitions**: use for depth/focus shifts, not as a crutch for cuts. *"foreground card sharpens from a soft blur as it comes into focus"*.
- **Opacity sequencing**: never fade everything at the same rate — stagger. *"cards fade in sequentially, each starting 80ms after the previous, 0→100% opacity"*.
- **Layer parenting**: describe hierarchical motion explicitly for multi-element scenes. *"the icon is parented to the card — as the card slides, the icon moves with it but rotates independently"*.
- **Constraint-based animation**: for elements that should react to each other. *"the glow follows the cursor position; the card tilts slightly toward the glow source (subtle parallax)"*.

## Reusable pattern: the "card reveal"

The single most common shot in this style. Formula:
1. Card starts at 90-95% scale, 0% opacity, offset 20-40px from resting position
2. Anticipation: near-zero hold (1-2 frames)
3. Slides + scales + fades to 100% simultaneously, ease-out-back curve
4. Settles with a 3-5% overshoot then rebounds to rest
5. Optional: subtle glow pulse on settle to mark arrival

Prompt phrasing: *"UI card slides up and scales in from 92% to 100%, fading in, ease-out-back with a soft overshoot settle."*

## Do / Don't

| Do | Don't |
|---|---|
| Name the easing curve explicitly | Say "smoothly animates" with no curve specified |
| Stagger multi-element reveals | Animate 4+ elements simultaneously at identical timing |
| Anchor motion to a clear start/end state | Describe open-ended continuous motion with no resolution |
| Keep secondary motion subtle (low amplitude) | Let background motion compete with the hero element |
