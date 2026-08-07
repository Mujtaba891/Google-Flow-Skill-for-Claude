# Camera Motion

Camera language for motion graphics differs from live-action — moves are smaller, slower, and more deliberate. A common AI-video tell is camera moves that are too large, too fast, or too "handheld" for what is meant to be a clean product piece.

## Core moves

- **Push-in / Pull-out (dolly)**: the workhorse move. Push-in draws attention to a detail (a metric, an icon); pull-out reveals context (a full dashboard). Keep it slow: 5-15% scale change over a 3-5s shot for a subtle push, reserve faster pushes (worth calling "snap-push") for punchy 1-2s feature beats.
- **Orbit**: for 3D/isometric objects — a slow arc around a floating object or UI stack, typically 15-30° of rotation over the shot, never a full 360 unless it's explicitly the hero shot.
- **Crane**: vertical camera move, used to transition between a "zoomed out" establishing view and a "zoomed in" detail view. Pair with a slight push for a natural feel.
- **Pan / Tilt**: horizontal/vertical reframing without moving position. Use sparingly and slowly in this style — whip pans belong to the fast-paced "promo burst" style only (see `visual_language.md`).
- **Parallax depth**: background, midground, and foreground layers move at different rates as the camera drifts — this is what makes flat UI compositions feel dimensional. Always specify at least 2 depth layers when describing a scene with a camera move.
- **Handheld simulation**: near-imperceptible organic drift (not shake) — used only when the brand tone wants "human" warmth rather than "precision tech." Default to NOT using this for SaaS/enterprise content.
- **Micro camera drift**: the default "resting" camera state for static-feeling shots — a near-imperceptible slow drift (1-3% over the whole shot) so the frame never feels dead. Almost every shot should have at least this much.

## Camera move selection by mood

| Brand tone | Preferred camera language |
|---|---|
| Enterprise / isometric-3D | Slow orbit, slow push, crane between layers |
| Dark-mode AI/dev tool | Linear dolly, precise (not floaty) push-ins, minimal pan |
| Bright/playful/consumer | Whip pans, fast snap-pushes, quick reframes |
| Fintech / banking | 3D object rotation (phone tilt), smooth dolly, no handheld |
| Growth/analytics dashboard | Continuous fluid pan along a path (e.g. following a chart line) |

## Rules

- Never combine more than one camera move type per shot unless one is subtle background drift (e.g. push + parallax drift is fine; orbit + whip pan is not).
- Camera moves should motivate a narrative beat — reveal, focus, or transition — not move for its own sake.
- End every camera move on a still (or near-still) frame if the next beat is a cut; end on continued drift if the next beat is a Flow "extend."
