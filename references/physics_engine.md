# Physics & Weight Simulation

AI video models don't run real physics, but describing motion *as if* real physics were involved is what makes it read as "believable" rather than "animated."

## Spring physics (the core model)
Describe UI motion using spring language: an element has **stiffness** (how fast it snaps to target) and **damping** (how much it oscillates before settling). In prompts:
- High stiffness, high damping → quick, precise, no overshoot ("snappy, no bounce")
- Medium stiffness, low-medium damping → the default premium feel: *"springs into place with a soft single overshoot, settles quickly"*
- Low stiffness, low damping → floaty, slow settle — reserve for large/heavy elements (full dashboard panels) or calm/enterprise brand tone

## Momentum
Elements that were already moving shouldn't stop instantly — describe a deceleration tail: *"the card continues its slide with decaying momentum before coming to rest"* rather than a hard stop.

## Overshoot & settle
The signature of "designed" motion: target value is passed by 3-8%, then eases back to rest in one small correction. More than one visible oscillation reads as cartoonish for SaaS content (reserve multi-oscillation elastic bounce for explicitly playful brand tone).

## Weight simulation by element type
| Element | Implied weight | Motion character |
|---|---|---|
| Small icon / button | Light | Fast, can have elastic bounce |
| Text / headline | Light-medium | Quick ease-out-back, minimal overshoot |
| UI card | Medium | Ease-out-back, single soft overshoot |
| Full dashboard panel / large 3D object | Heavy | Slower ease-in-out, minimal or no overshoot, more anticipation |
| Background/environment | Very heavy (near-static) | Continuous slow drift only, never a discrete "arrival" |

## Consistency rule
Once a weight/physics feel is established for an element type in scene 1, keep it consistent across the whole sequence — a card that springs playfully in scene 1 shouldn't suddenly move with heavy, damped motion in scene 3 unless there's a deliberate tonal shift (e.g. transitioning from playful intro to serious data reveal).
