# UI-Specific Animation Patterns

## Dashboard reveals
Cards enter staggered (80-150ms apart), each following the `animation_rules.md` "card reveal" pattern. Charts/graphs should never appear fully formed — bars grow from baseline, lines draw on left-to-right, numbers count up rather than snapping to final value.

## Toggle switches
Instant-feeling but not linear — use expo easing over 0.15-0.2s, with a small glow-color-shift on the "on" state landing.

## Metric/counter animations
Numbers counting up should decelerate into the final value (ease-out), never count at constant speed. Pair with a small scale-pop (102%→100%) on arrival at the final number.

## Chart/graph draw-on
Line charts: draw on via trim-path left-to-right, ease-out, with the line's leading edge showing a small glow/dot marker. Bar charts: bars grow from baseline with staggered start times (left-to-right), ease-out-back for a slight overshoot on height.

## Card stacking / carousel
Cards should overlap with clear depth cues (drop shadow increasing with "closer" cards, slight scale difference 2-4% between depth layers). Stack shuffling motion: outgoing card slides down/back and fades while incoming card slides up/forward — never a flat crossfade.

## Search bars / command palettes
Cursor blink should be a subtle secondary detail, never the focal motion. Typing animation (if shown) should have natural, slightly uneven character timing rather than perfectly uniform intervals — uniform typing reads as robotic.

## Notification / badge pop-ins
Small amplitude elastic easing is appropriate here (unlike most SaaS UI motion) — a badge/notification should feel like it "catches" attention with a quick spring-pop.

## Theme transitions (dark↔light)
Cross-fade the background/surface colors while UI content (icons, text) holds its layout — never move UI elements during a theme transition, isolate the change to color/luminance only, over 0.4-0.6s ease-in-out.
