---
name: google-flow-motion-graphics
description: Generate premium SaaS/product explainer motion graphics prompts and shot sequences for Google Flow (and other text-to-video tools like Veo, Wan2.1, HunyuanVideo, Runway, Kling). Use this skill whenever the user asks to create, storyboard, prompt, or refine an AI-generated motion graphics video, product explainer, app demo animation, UI animation, kinetic typography sequence, or SaaS promo video — even if they just describe a product and ask for "a video" or "an animation" without naming Google Flow explicitly. Also use when the user asks to critique, improve, or debug an existing AI video generation prompt, build a scene-by-scene shot list, choose camera moves/easing/transitions for a motion graphic, or wants a dataset/style-guide for training or briefing an AI video model on modern SaaS motion design. Covers motion principles, camera language, color/lighting, typography motion, transitions, easing curves, scene structure, and negative prompting specific to this visual style.
---

# Google Flow Motion Graphics Skill

This skill turns a product idea (or a rough brief) into shot-by-shot, prompt-ready motion graphics sequences in the modern "SaaS explainer" visual language: dark/light UI dashboards, glowing gradient orbs, floating cards, kinetic typography, isometric 3D, glass/neon accents, snappy spring-eased motion.

It is built for **Google Flow** (Google's AI filmmaking tool built on Veo), but the underlying theory works for any text-to-video model — Veo, Wan2.1, HunyuanVideo, CogVideoX, Runway, Kling, AnimateDiff. Flow-specific mechanics (scene extension, ingredients-to-video, camera controls) are called out where they matter.

## When to go deeper vs. answer directly

For a single quick prompt ("give me a prompt for a glowing dashboard reveal"), you usually don't need to open every reference file — pull from `prompt_templates.md` and `easing_library.md` directly. For anything with multiple scenes, a full explainer, a style guide request, or "make this feel more premium," read the relevant reference files below before writing — the specifics (exact easing curves, camera presets, negative rules) are what separate a generic AI video from one that reads as professionally directed.

## Workflow

1. **Clarify the brief** (only if genuinely missing — don't block on this): product/brand, mood (e.g. dark-mode tech vs. bright/playful vs. enterprise/isometric), video length, aspect ratio (16:9 landscape, 9:16 vertical/Reels, 1:1), and whether this is one continuous shot or a multi-scene sequence.
2. **Pick a scene structure** — see `scene_structure.md` for the Hook → Reveal → Focus → Transformation → Explanation → Climax → Outro arc and shorter variants for 6–15s clips.
3. **Design each shot**: for every scene decide (a) what moves first, (b) what stays static as an anchor, (c) camera move (`camera_rules.md` + `camera_presets.json`), (d) easing (`easing_library.md` + `animation_curves.json`), (e) color/lighting (`color_theory.md`, `lighting_rules.md`), (f) transition into the next scene (`transition_library.md` + `transitions.json`).
4. **Write the prompt** using `prompt_templates.md` as the structural pattern — trigger/style words first, then subject, then camera, then motion/easing, then lighting, then a closing quality tag.
5. **Apply negative rules** from `negative_rules.md` — these prevent the most common AI-video tells (robotic linear motion, jittery cameras, over-animation).
6. **Run the `quality_checklist.md`** before handing the prompt(s) back to the user.

## Reference files

| File | Read this for |
|---|---|
| `references/motion_principles.md` | Disney's 12 principles adapted for UI/motion graphics — anticipation, overshoot, follow-through, rhythm, visual weight |
| `references/animation_rules.md` | Property-level animation system: scale, position, rotation, morph, trim paths, mask reveals, layer parenting |
| `references/camera_rules.md` | Camera language: push/pull, dolly, orbit, crane, parallax, handheld sim, micro-drift |
| `references/camera_presets.json` | Named, ready-to-use camera move presets with prompt phrasing |
| `references/composition_rules.md` | Rule of thirds, negative space, focal point, grid systems, layer depth |
| `references/color_theory.md` | Premium color combos, contrast ratios, gradients, glassmorphism/neon/dark-UI palettes, emotional color mapping |
| `references/color_palettes.json` | Named palettes ready to drop into prompts |
| `references/typography_motion.md` | Kinetic type: word/character reveals, mask reveals, reading rhythm, font pairing |
| `references/transition_library.md` | Swipe, morph, zoom, whip, liquid, blur, match-cut, shape transitions |
| `references/transitions.json` | Transition presets with timing and prompt phrasing |
| `references/easing_library.md` | Full easing vocabulary (ease in/out, back, elastic, bounce, expo, etc.) and when to use each |
| `references/animation_curves.json` | Cubic-bezier values for each named easing |
| `references/physics_engine.md` | Spring physics, momentum, overshoot/settle, weight simulation for "believable" UI motion |
| `references/scene_structure.md` | Scene arcs (Hook→Outro), timing/pacing by video length |
| `references/scene_templates.json` | Ready-made scene sequences for common video types (feature teaser, app launch, AI agent demo, dashboard analytics) |
| `references/ui_animation.md` | Dashboard/card/toggle/chart-specific animation patterns |
| `references/object_animation.md` | 3D object, isometric grid, and product-shot animation patterns |
| `references/lighting_rules.md` | Ambient/rim lighting, glow intensity, bloom thresholds, glass reflections |
| `references/rendering_style.md` | Render/finish descriptors (glass, matte, neon-glow, soft-shadow) and how to phrase them |
| `references/visual_language.md` | Overall design language checklist — how the 9 reference clips' styles differ and when to use each |
| `references/negative_rules.md` | What to explicitly avoid/negative-prompt — robotic movement, linear interpolation, random shake, over-animation |
| `references/prompt_templates.md` | The structural prompt formula + filled examples for Google Flow |
| `references/quality_checklist.md` | Pre-delivery checklist |
| `references/motion_patterns.json` | Reusable named motion patterns (card-stack-reveal, orbit-node-branch, etc.) |
| `references/training_examples.json` | Full annotated example prompts, one per reference-clip style, for few-shot grounding |

## Source grounding

The style patterns in this skill (color combinations, timing, layer ordering, camera philosophy) were extracted from analysis of 9 professionally produced SaaS/app explainer clips spanning: kinetic-typography product reveals, dashboard/growth explainers, dark-mode chatbot promos, isometric enterprise-tech explainers, multi-agent AI demos, bold promo-burst showcases, mobile banking app launches, node/flowchart AI-workflow explainers, and command-palette feature teasers. Each style is catalogued in `visual_language.md` so you can match a new brief to the closest precedent.

## Output format

Default to giving the user: a numbered scene list (1 line of *creative intent* per scene) followed by the actual Flow-ready prompt text for each scene in a code block, so they can copy-paste directly. For multi-scene sequences, note where Flow's "extend" feature can chain shots vs. where a hard cut/transition is better.
