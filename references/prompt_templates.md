# Prompt Templates for Google Flow

## Structural formula
```
[style/trigger words], [subject + key UI/visual elements], [camera movement],
[motion + easing description], [lighting/color], [rendering finish],
[quality/production tag]
```

Keep style words first (they anchor the model's overall aesthetic decisions before it processes specifics), and always name easing curves explicitly rather than using vague adverbs.

## Filled example — Dashboard/growth explainer style
```
Modern SaaS motion graphics, clean vector dashboard animation, dark green-to-black
gradient background, a glowing lime-green metric chart card scales up from 92% to
100% and slides up from below frame, ease-out-back with a soft overshoot settle,
camera slowly pushes in 8% over the shot with a gentle parallax drift on the
background particles, single glowing star particle drifts slowly in the upper right,
soft diffused shadow beneath the card, professional SaaS product advertisement,
premium motion design, high production value.
```

## Filled example — Isometric enterprise-tech style
```
Modern SaaS motion graphics, isometric 3D cube grid assembling tile by tile from
back to front, deep blue background, each cube scales in from 0 with ease-out-back,
40ms stagger between tiles, consistent top-left light source and isometric
perspective across all elements, camera slowly orbits 20 degrees around the grid,
ease-in-out, subtle cyan glow along cube edges, soft bloom limited to the brightest
edge highlights only, professional enterprise technology advertisement, premium
motion design.
```

## Filled example — Kinetic typography hook (short/teaser)
```
Modern SaaS motion graphics, kinetic typography reveal, bold geometric sans-serif
headline "Automate Everything" revealed word by word with 120ms stagger, ease-out-
back scale pop on each word, dark near-black background with a single soft violet
glow behind the final word, camera holds steady with only micro-drift, no shake,
professional product advertisement, high production value.
```

## Multi-scene sequence prompting (Flow-specific)
For Flow's scene-extension feature: end each prompt describing a settled final frame (not mid-motion) if the next clip is a hard cut, or describe continued camera/element motion if you intend to extend the same clip. When extending, restate the locked style/palette/lighting words at the start of the next prompt even though it's a continuation — this keeps consistency across generations.

## Adapting a template
1. Pick the closest `visual_language.md` style as your base
2. Swap in the specific product/UI details from the brief
3. Choose camera move from `camera_rules.md` matched to brand tone
4. Choose easing from `easing_library.md` matched to the element's implied weight
5. Add one negative-rule check pass before finalizing (`negative_rules.md`)
