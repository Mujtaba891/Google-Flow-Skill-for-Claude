# Rendering Style / Finish Descriptors

Vocabulary for describing the final "look" of a render — use 2-4 of these per prompt, not the whole list.

- **Glass / glassmorphism**: translucent panels, blur backdrop, thin light borders
- **Matte**: flat, non-reflective surfaces, good for calm/minimal enterprise content
- **Neon-glow**: saturated color at high luminance with visible bloom
- **Soft-shadow / diffused**: large-radius, low-opacity shadows for depth without harshness
- **Metallic**: subtle specular highlights on card/object edges, reads as premium/fintech
- **Gradient-mesh**: smooth multi-directional color blends for backgrounds
- **Clean vector**: flat-shaded, minimal gradient, high clarity — good for growth/dashboard content
- **Photoreal-UI-composite**: UI elements rendered with realistic depth/shadow as if physically photographed on a surface — good for product/device-launch content
- **Cinematic depth-of-field**: background softly out of focus behind a sharp hero element, reinforces focal hierarchy

## Combining descriptors
Pick a primary finish (glass, matte, or clean-vector) and at most one secondary modifier (neon-glow, metallic, or cinematic-DOF). Combining more than two finish descriptors tends to confuse the model and produce an inconsistent look across a sequence.

## Quality/production tags
Close prompts with a short quality anchor: *"professional SaaS product advertisement, high production value, premium motion design"* — this consistently improves polish in Flow/Veo-class models without being an empty buzzword dump (keep it to one short clause, not a wall of quality adjectives).
