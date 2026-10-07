# Jurgen Donner: Visual Spec

## The principle

The look is the hook. People should stop scrolling because something is off, then stay because they cannot decide if he is real.

That only works if he looks **photoreal and lo-fi**, not polished. Glossy, perfectly lit, shallow-depth-of-field footage reads as AI instantly. Grainy phone footage under a bad fluorescent light reads as a real weird uncle. So we spend realism on the boring parts (skin, lighting, clutter, camera) and put the weirdness in a few specific details.

**Real:** skin pores, liver spots, slightly uneven teeth, a stained shirt collar, messy cables, bad lighting, a phone camera.
**Wrong:** the orange gloves, the haircut, the monocle-glasses, Klaus.

## The look (lock this, never change it)

- **Build:** very tall (about 196 cm) and thin, slightly stooped from decades of bending over workbenches. Long bony hands.
- **Face:** long and narrow, deep-set pale blue eyes, prominent hooked nose, clean-shaven, deep lines around the mouth. Expressive.
- **Eyebrows:** enormous, white, bushy, flaring upward at the ends. They do most of his acting.
- **Hair:** white, severe, perfectly slicked side part with a comb line visible. Above the left ear there is a rectangular patch about the size of a matchbox where the hair is singed short and slightly darker. Old explosion. Never explained.
- **Glasses:** small round wire-frame glasses. A jeweler's magnifying loupe is clipped to the right lens and flips up and down. Usually flipped up; flipped down when he examines something closely.
- **Clothing:** white dress shirt buttoned all the way to the top, no tie. Over it, a pale gray knitted wool vest (sleeveless). Brown corduroy trousers.
- **Gloves:** bright safety-orange rubber gloves, elbow length. Always on. This is the brand color. Every thumbnail and first frame should have orange in it.
- **Optional:** a pencil behind his ear.

The silhouette test: someone who has seen three videos should recognize him from a 1-second blurred thumbnail. Orange gloves, tall thin frame, slicked white hair, giant eyebrows.

## The lab (main set)

- Low concrete basement, gray walls, one flickering fluorescent tube light overhead (slightly green tint).
- Pegboard wall of hand tools behind him, each tool outlined in marker.
- A green chalkboard covered in equations, plus one line clearly not math ("HELGA LIES" partly erased).
- An old 1990s CRT television on a cart. **This is the reaction device:** he watches clips on the CRT, taps the glass with an orange finger, leans in with the loupe down.
- A workbench with half-built devices, a soldering iron, a coffee mug reading "No. 1 Inventor" that he bought himself.
- Klaus's charging dock in the corner, with a tiny hand-lettered sign: "KLAUS".

## Camera style

- Shot as if on an old phone propped on the workbench: slight wide-angle distortion, a little grain, auto-exposure flicker from the fluorescent light.
- He sits slightly too close to the camera.
- Vertical 9:16. Head and shoulders for talking; wider for memes and dancing.
- No cinematic lighting, no bokeh, no color grading. If it looks like a film, it is wrong.

## Klaus

Round dark-gray robot vacuum, two large googly eyes glued on top (slightly crooked), a small gray hand-knitted wool hat with a pompom. Scuffed from hitting furniture.

## Generation workflow (consistency)

1. **Make a reference sheet first.** Generate Jurgen front, three-quarter, and profile, plus three expressions (outraged, delighted, squinting through loupe). Pick the best, then never regenerate him from scratch. Every later image and video uses these references.
2. **Use reference-image features** in whatever tool you use (character reference, image-to-video starting frames, or a trained LoRA). Text prompts alone will drift.
3. **Generate start frames as images, then animate.** Image first, video second. It keeps the face consistent.
4. **Lip-sync last.** Generate the voice line, then lip-sync it onto the clip.
5. Review every clip for drift: gloves must be orange, singed patch on the left, loupe on the right lens. Reject any clip where these flip.

## Master prompt (base for every image)

> Photorealistic candid smartphone photo, vertical 9:16. A very tall thin 67-year-old German man with a long narrow face, deep-set pale blue eyes, hooked nose, clean-shaven, deep wrinkles, and enormous bushy white upward-flaring eyebrows. White hair slicked into a severe side part, with a small rectangular singed patch above the left ear. Small round wire-frame glasses with a jeweler's loupe clipped to the right lens, flipped up. White dress shirt buttoned to the top, no tie, pale gray knitted wool vest. Bright safety-orange elbow-length rubber gloves. Concrete basement workshop, pegboard of outlined tools, green chalkboard with equations, harsh flickering fluorescent overhead light with a slight green cast. Slight wide-angle phone lens distortion, visible grain, natural skin texture with pores and age spots. Amateur, unposed, not cinematic.

Append the scene: what he is doing, expression, and props (CRT TV, Klaus, etc.).

## Thumbnail and first-frame rules

- Orange visible in the first frame, always.
- His face fills at least a third of the frame, mid-expression (never neutral).
- One weird detail readable at phone size: loupe down, Klaus in frame, something smoking on the workbench.
