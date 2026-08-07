# Color Intelligence

## Premium combinations observed across reference styles
- **Dark-mode tech**: near-black background (#0A0A0F to #121218) + one saturated accent (neon green, electric orange, or violet) + white/off-white text. Never more than one saturated accent color per scene.
- **Growth/analytics**: dark green-to-black gradient background + a single bright accent (yellow-green or lime) for the "growth" signal (charts, star particles) — the accent should map to the concept of positive movement.
- **Enterprise/isometric**: deep blue base + cyan/white glow highlights — communicates trust and scale, avoid warm colors entirely in this mode.
- **Bright/consumer/promo**: white or very light background + one or two bold saturated colors used at high area-coverage (not just accents) — this is the exception to "one accent color," used specifically for high-energy promo-burst content.
- **Fintech/banking**: deep gradient (navy-to-black or purple-to-black) + metallic/white card surfaces + a single brand accent, communicates premium/secure.

## Contrast ratios
Text over any background must maintain strong perceptual contrast even as backgrounds animate — when prompting a gradient background behind text, specify *"background gradient stays dark enough to keep white text at high contrast throughout"* to prevent the model from washing out legibility mid-animation.

## Gradient construction
Two-stop gradients read as more premium than three+ stop rainbow gradients. Angle gradients diagonally (135°) by default for a sense of motion even in static frames. Radial gradients (glowing orb effect) should have a soft, wide falloff — not a hard-edged circle.

## Glassmorphism palette
Semi-transparent white/light panels (8-15% opacity) over a colorful blurred background, thin 1px light borders, soft drop shadow. Prompt phrase: *"frosted glass UI panel, translucent with soft blur backdrop, thin light border."*

## Neon palette
Saturated color at high luminance against near-black, always paired with a glow/bloom effect (see `lighting_rules.md`). Limit to 1-2 neon colors per scene — competing neons read as cheap rather than premium.

## Dark UI palette
True dark-gray/near-black bases (avoid pure #000000, which crushes on most displays — use #0A0A0F to #16161C range), layered with slightly-lighter-gray card surfaces (#1C1C24 range) for depth without color.

## Emotional color mapping
| Feeling to convey | Color direction |
|---|---|
| Trust, scale, enterprise | Deep blue, cyan |
| Growth, positivity | Green, lime |
| Innovation, AI | Violet, electric purple, orange |
| Premium, secure (fintech) | Near-black + metallic/white |
| Energy, consumer excitement | Bold saturated multi-color on white |
