# REVIEW — first-video

## Creative calls
- No topic was given, so the film is about HyperFrames itself, in Hebrew: "כותבים HTML → מקבלים וידאו → כל רינדור — אותו סרט → HyperFrames".
- Look: a Swiss screen-print poster. Flat signal yellow `#F2C12E`, ink `#111111`, one ultramarine accent `#2340E0`, Heebo 900/500 (OFL, shipped in `assets/fonts/`), JetBrains Mono for code. Text is right-aligned (RTL); code and film run left to right.
- 12.6 s at 1920×1080, 30 fps, silent. The film is under 15 s, so it has no music. Add a bed through `/media-use` if you want one.
- Storylines not built: a product promo (no product was named) and a bouncing-ball character short.

## Measured vs. looked at
- `hyperframes check`: 0 errors, 0 warnings across lint, runtime, layout, motion, contrast and craft.
- Looked at: the review sheets (beats, both seams, phone width) and frames pulled from the rendered MP4.
- Render: `renders/first-video.mp4`, H.264, 378 frames, 12.6 s, 1.3 MB.
- Not checked: there is no sound to measure.

## Weakest shot
- The film-strip beat (3.2–6.4 s). The ball's position changes from frame to frame and reads as a bounce, but only if you look closely. With more time I would give it a larger arc, or squash and stretch, so the sequence reads at a glance.
- The code lines in shot 1 (38 px) are small at phone width. They illustrate the idea and are not meant to be read word for word.

## Kept on purpose
- `data-layout-allow-overflow` on `#strip-a` / `#strip-b`: the film runs past the canvas by design.
- The blue flood in `compositions/frames.html` uses hard-coded hex values (`#F2C12E → #2340E0`). Change them there if you re-brand. Every other colour comes from the root variables.

## Editing
- Copy is in variables (Studio → Variables): headlines per scene, the counter label, the end title and subline.
- `compositions/frames.html` was generated from a small script; editing the HTML directly is fine.
