# Professional Easing Library

The single highest-leverage lever for making AI-generated motion look designed. Always name a specific curve in prompts — never say "smoothly" or "gradually" alone.

| Curve | Feel | Best for |
|---|---|---|
| **Ease In** | Slow start, accelerates | Exits, elements leaving frame |
| **Ease Out** | Fast start, decelerates into rest | Entrances, the default for most UI reveals |
| **Ease In-Out** | Slow-fast-slow | Camera moves, background/ambient motion |
| **Back** (ease-out-back) | Overshoots slightly past target then settles | Card reveals, buttons, anything that should feel "snappy" and alive |
| **Elastic** | Springs past target with 1-2 oscillations before settling | Playful/consumer brand moments, notification pop-ins — use sparingly in enterprise content |
| **Bounce** | Settles with a literal bounce (like a dropped ball) | Rare in SaaS UI — reserve for explicitly playful/gamified brand tone |
| **Quart / Quint** | Increasingly sharp acceleration curves | Fast whip-style transitions, promo-burst pacing |
| **Expo** | Extremely sharp, near-instant then holds | Snap-zooms, instant state changes (toggle flips) |
| **Circ** | Circular-arc-shaped velocity curve | Natural-feeling rotations, orbit camera moves |
| **Cubic** | General-purpose smooth curve | Safe default for anything not covered above |

## When each is used (by scene role)
- Hero card/text entrance → **ease-out-back**
- Camera drift/push → **ease-in-out** or **circ**
- Toggle/switch flip, instant UI state change → **expo**
- Exit/dismiss → **ease-in**
- Notification, playful micro-interaction → **elastic** (small amplitude only)
- Chart line draw-on, progress fill → **ease-out** or **linear-with-ease-out-tail** (never pure linear — see `negative_rules.md`)

See `animation_curves.json` for cubic-bezier numeric values to reference or hand to a compositing tool if the user is also doing manual finishing work.
