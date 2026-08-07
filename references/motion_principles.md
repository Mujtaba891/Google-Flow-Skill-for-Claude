# Motion Principles

Disney's 12 principles of animation, adapted for UI/motion graphics and AI text-to-video prompting. These are the "why" behind every other file in this skill — reference them when a generated clip feels "off" but you can't say why.

## The adapted 12

1. **Squash & Stretch → Elastic Response.** UI elements shouldn't deform physically, but they should compress slightly on impact and rebound — a card that "lands" scales to 0.96 then springs to 1.0. Prompt phrase: *"subtle elastic settle on landing"*.
2. **Anticipation.** Nothing should move without a micro-beat of preparation — a card that's about to slide in first dims/shrinks slightly, a button about to trigger an action pulses once. Without this, motion reads as robotic. Prompt phrase: *"brief anticipation beat before [action]"*.
3. **Staging.** Only one thing should command attention per moment. If text is animating in, background elements hold still or drift almost imperceptibly. Never animate the hero element and three background elements with equal intensity simultaneously.
4. **Straight Ahead vs. Pose-to-Pose.** For AI video, think pose-to-pose: define the key state (start UI layout, end UI layout) and let the model interpolate — this is more reliable than describing continuous free-form motion.
5. **Follow-Through & Overlapping Action.** When a card group moves, elements don't arrive simultaneously — the container leads, inner content follows 1-3 frames later ("staggered reveal"). Prompt phrase: *"staggered follow-through, container leads content by a beat"*.
6. **Slow In / Slow Out (Easing).** Nothing in premium motion design moves at constant (linear) speed. See `easing_library.md` — this is the single highest-leverage principle for making AI video look "designed" rather than "generated."
7. **Arcs.** Motion paths curve, they don't move in straight robotic lines — a card sliding into place travels a gentle arc, a camera push has a hint of curvature rather than a dead-straight dolly.
8. **Secondary Action.** Supporting motion that reinforces the main action without competing — a glow pulse behind a headline as it reveals, particle drift behind a hero card. Keep secondary action at 20-40% the visual intensity of the primary action.
9. **Timing.** Fast = energetic/snappy (SaaS feature reveals, 0.2-0.4s), slow = premium/calm (enterprise/isometric explainers, 0.6-1.2s). Match timing to brand tone before anything else.
10. **Exaggeration.** A little overshoot on scale/rotation reads as "designed," not "buggy" — 3-8% overshoot past the resting value, then settle. More than that reads as cartoonish for SaaS content.
11. **Solid Drawing → Spatial Consistency.** 3D/isometric elements must maintain consistent perspective and light direction across a scene. Call this out explicitly in prompts for multi-shot sequences: *"maintain consistent isometric perspective and light source throughout."*
12. **Appeal.** Every hero element (headline, key metric, CTA) should have one deliberate "moment" — a glow, a scale pop, a color shift — that a viewer's eye is drawn to. Not everything can be appealing; that's what makes the hero appealing.

## Motion hierarchy (what should move first)

In a typical SaaS explainer scene, the priority order is:
1. Background environment (gradient shift, particle drift) — starts first, most subtle, continues throughout
2. Camera move — starts near-simultaneously with background, very gradual
3. Hero UI element / headline — enters with the clearest, most deliberate motion
4. Supporting elements (secondary cards, icons, metrics) — staggered in after the hero, 0.1-0.3s delay each
5. Micro-details (cursor blinks, particle sparkles, glow pulses) — continuous, low-amplitude, never the focal point

## Visual momentum & rhythm

Cut/scene length should follow a rhythm, not be uniform. Typical pattern for a 20-30s explainer: longer establishing scene (3-4s) → 2-3 quicker feature beats (1.5-2.5s each) → one lingering "hero" moment (3-4s) → quick outro (1.5-2s). Uniform-length scenes are the fastest way to make an AI video feel like a slideshow rather than a directed piece.
