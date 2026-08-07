# Scene Construction

## The full arc (for 25-40s explainers)
1. **Hook** (1.5-3s) — a striking, simple visual that states the category/promise without detail. Often a logo/wordmark kinetic reveal or a single glowing hero element.
2. **Reveal** (3-4s) — the product itself appears (dashboard, app screen, agent interface). Camera pulls back or pushes in to establish context.
3. **Focus** (2-3s per beat, x2-3 beats) — individual feature call-outs, one per shot. This is where most "feature list" content lives.
4. **Transformation** (2-4s) — a before/after or state-change moment (empty→full dashboard, manual→automated, chaos→organized) — the emotional core of most SaaS explainers.
5. **Explanation** (2-3s per beat) — supporting detail/metrics/proof points, often paired with kinetic typography stats.
6. **Climax** (3-4s) — the single most visually impressive shot in the piece — the "hero shot" the whole video builds to.
7. **Outro** (1.5-2.5s) — logo/CTA, calm and simple, mirrors the Hook's visual language to bookend the piece.

## Shorter formats
- **6-10s teaser** (social/ads): Hook → Climax → Outro only. Cut Focus/Explanation entirely.
- **15s feature spot**: Reveal → one Focus beat → Outro.
- **60s+ deep-dive**: full arc above, with 2-4 Focus beats and 2-3 Explanation beats instead of 1 each.

## Pacing rule
Avoid uniform scene lengths — see `motion_principles.md`'s "visual momentum" section. As a rule of thumb, no two consecutive scenes should be within 0.3s of the same length.

## Consistency rules across a scene sequence
- Lock color palette and lighting direction across all scenes (see `visual_language.md`) unless a deliberate mode-shift (e.g. dark→light theme transition) is part of the narrative.
- Lock the "physics feel" (see `physics_engine.md`) across scenes of the same type.
- If using Flow's scene-extension/continuation feature, end each generated clip on a frame that naturally motivates the next prompt (a settled state, not mid-motion) unless doing a camera match-cut.

## Randomization limits
Vary micro-details (exact particle positions, minor timing offsets) freely — this is where AI generation should be allowed to improvise. Do NOT vary macro structure (palette, camera philosophy, easing character, layer depth count) between scenes in the same sequence; lock those explicitly in every prompt.
