# SPEC — "מקוד לסרט" (From code to film)

GOAL:    In 12.6 s the viewer gets the whole idea of HyperFrames: you write HTML, it becomes video
         frame by frame, and every render comes out identical. The film ends on the name.
OUTPUT:  HyperFrames, 1920 x 1080, 30 fps, no audio (under 15 s, no voice).
TIME:    12.6 s x 30 = 378 frames. Scenes: code 0–96, frames 96–288, endcard 288–378.

LOOK:    Swiss screen-print poster: flat planes, hard edges, no gradients, no shadows, no glow.
         ground   #F2C12E signal yellow, flat (blue flood #2340E0 for the "identical" beat only)
         ink      #111111 for every reading word, the code slab and the film band
         accent   #2340E0 ultramarine: one focus per frame ("HTML", the frame number, "Frames")
         paper    #F6F1E6 inside the film frames and code attributes only
         display  Heebo 900 (Hebrew + Latin, assets/fonts), headlines 150 px / 104 px / 230 px, tracking -2%
         body     Heebo 500, 48–60 px
         code     JetBrains Mono 400, 38 px, line height 60 px
         Text is right-aligned to the title-safe edge x = 1728 (RTL); code and film run LTR.
OBJECTS: a code slab (black rectangle with five lines of real HyperFrames HTML);
         a film strip (black band, sprocket holes punched through to the ground, 16:9 paper frames,
         each holding one frame of a bouncing ball, so the row reads as consecutive frames);
         a frame counter (Hebrew label + three-digit mono number).
MOTION:  enter expo.out / power4.out; morph and flood power3.inOut / power2.inOut; exit and whip power3.in;
         typing = steps(chars) on clip-path, 0.02 s a character; film travel linear (constant speed is the point);
         titles land and hold dead still; exits 0.15–0.2 s blur-out.
SHOTS:
  1. f0–96   code: the slab whips in from the left (x −300 → 0, blur 14 → 0, 0.55 s) and types five lines.
             "כותבים" / "HTML" (accent) blur in on the right, then "קוד רגיל, בדפדפן רגיל".
             Hand-off: text blurs out, the slab grows into the film band (object becomes the world, 0.6 s).
  2. f96–192 frames: the band punches its sprocket holes, frames build in, the strip travels right.
             "מקבלים וידאו" lands top right; the counter "פריים 001 → 180" counts under the band.
             Hand-off: colour flood to ultramarine (0.4 s) while the strip stays.
  3. f192–288 identical: strip A lifts and scales to 0.78, strip B (the second render) rises in below,
             moving in perfect sync. "כל רינדור — אותו סרט" + "גם בשני, בשלישי ובמאה".
             Hand-off: whip, both strips accelerate off right with 16 px blur; cut on the fastest frame.
  4. f288–378 endcard: "HyperFrames" ("Frames" in accent) lands from the left blurred and sharpens,
             "הסרטון הראשון של הפרויקט" blurs in under it; holds 2 s dead still to the end.
BANNED:  dark void ground; glow, bloom, particles; gradients on grounds; glass cards; pills and chips;
         everything centred; everything fading and sliding up; floating or pulsing loops on titles;
         corner labels or HUD decoration; logo docked in a corner; three cards in a row.
QA:      f0 (slab visible, not empty); f60 (code typed, headline read); f94–f98 (morph seam matches);
         f150 (counter mid-count, frames readable); f240 (two strips in sync on blue); f286–f290 (whip cut);
         f377 (end card legible, still).
