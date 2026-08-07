# Negative Rules (What to Avoid)

Explicitly guard against these — either by negative-prompting where the tool supports it, or by describing the *correct* alternative behavior positively (more reliable in Flow/Veo-class models than bare negatives).

- **Avoid robotic/linear movement** → always specify an easing curve (see `easing_library.md`); never leave motion undescribed or say "moves smoothly" alone.
- **Avoid pure linear interpolation** → same fix as above; linear motion is the #1 tell of unpolished AI/motion-graphics output.
- **Avoid random/unmotivated camera shake** → specify camera stability explicitly for non-handheld styles: *"camera holds steady with only micro-drift, no shake."*
- **Avoid excessive glow/bloom** → cap glow to hero elements only (see `lighting_rules.md`); say *"glow limited to [specific element]"* rather than leaving it open.
- **Avoid abrupt stops** → every motion needs a settle/decay, not a hard stop — see `physics_engine.md` momentum rules.
- **Avoid conflicting motion directions** → if the camera pushes in, elements shouldn't simultaneously scale down (fighting the push); check that all simultaneous motions in a shot reinforce rather than cancel each other's implied direction.
- **Avoid color clashes** → max one saturated accent color per scene outside the bright/promo-burst style (see `color_theory.md`); check any multi-accent request against `visual_language.md`.
- **Avoid over-animating every element** → enforce the motion hierarchy from `motion_principles.md` — background/secondary elements should be visibly calmer than the hero element, not equally active.
- **Avoid uniform timing** → no two consecutive elements or scenes should animate/cut at identical duration (see `scene_structure.md` pacing rule).
- **Avoid text that's illegible mid-motion** → don't animate text with heavy blur/fast movement for longer than ~0.3s; it must be static and readable for the majority of its on-screen time.
- **Avoid describing more than ~4-5 distinct elements in one shot** → split into multiple scenes instead (see `composition_rules.md` negative-space rule).
- **Avoid mixing more than one camera move type per shot** (excluding subtle background parallax) — see `camera_rules.md`.
