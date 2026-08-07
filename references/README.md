# Motion Graphics Dataset — Google Flow Edition

Reference documentation for prompting AI video/motion-design generation tools (Google Flow, Veo, and text-to-video diffusion models generally) in the modern SaaS/product explainer visual style.

This is the supporting `references/` content for the `google-flow-motion-graphics` skill — see `../SKILL.md` for the entry point, workflow, and file index. Read this README if you're browsing the dataset directly rather than via the skill.

## What's here
18 markdown reference files covering motion principles, animation mechanics, camera language, composition, color, typography, transitions, easing, physics/weight, scene structure, UI-specific and 3D-object-specific patterns, lighting, rendering finish, overall visual language across 9 grounding styles, negative rules, prompt templates, and a quality checklist — plus 7 JSON files with structured, ready-to-drop-into-prompts presets (motion patterns, palettes, easing curves, transitions, scene templates, camera presets, and annotated training examples).

## How it was built
The style patterns (color combinations, timing, layer ordering, camera philosophy) were extracted from analysis of 9 professionally produced SaaS/app explainer video clips, then organized against established motion-design theory (Disney's 12 animation principles, standard easing/spring-physics vocabulary) and written up as prompting guidance specifically for Flow/Veo-class text-to-video generation.

## Quick start
For a one-off prompt, go straight to `prompt_templates.md` + `easing_library.md`. For a full explainer video, follow the workflow in `../SKILL.md`.
