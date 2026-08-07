# Typography Motion (Kinetic Type)

## Reveal patterns
- **Word-by-word reveal**: each word fades/scales in sequentially, 80-150ms stagger between words. Best for headline statements — matches natural reading rhythm.
- **Character animation**: individual letters animate in (common for logos, short punchy words). Use tighter stagger (20-40ms per character) and smaller motion amplitude than word-level reveals.
- **Mask reveal**: text is revealed by a moving wipe/mask rather than moving itself — reads as more "designed"/premium than elements flying in. Prompt phrase: *"headline revealed by a soft-edged left-to-right wipe mask."*
- **Scale reveal**: text pops from 85-95% to 100% scale with ease-out-back — good for single short statements/stat callouts.

## Reading rhythm
On-screen text needs to hold long enough to read comfortably: minimum ~0.3s per word of hold time after the reveal completes, before it starts exiting or the scene cuts. Don't let text finish animating in and immediately start animating out — this is one of the most common AI-video pacing failures.

## Motion blur
A touch of directional motion blur on fast text moves sells speed and weight — but only on the fastest reveals (promo-burst style); premium/enterprise text motion should stay blur-free and precise.

## Font pairing (descriptive, for prompting)
Since text-to-video models can't take exact font files reliably, describe typographic character instead: *"clean geometric sans-serif, bold weight for headline, medium weight for supporting text"* or *"rounded modern sans-serif with generous letter spacing"* for a friendlier tone. Keep to 2 weight levels max per scene (bold headline / regular body) — avoid describing more than one typeface family.

## Kinetic typography as the hero
When type is the primary subject of a scene (not overlaid on UI), give it the full motion-principle treatment from `motion_principles.md`: anticipation before reveal, overshoot on scale, staggered follow-through between words, and a clear single focal moment (usually the boldest/last word).
