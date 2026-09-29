
# Taare Twinkle Kyun Karte Hain? Â· Full Prompt Pack

Run order: **A â†’ B â†’ C â†’ V** (V needs the C frames). Paste each batch into its own agent session.

---

## BATCH A Â· Solid cutouts Â· PNG Â· pure white BG

```
You are an image generation agent. Work in TWO PHASES. Do not start Phase 2 until every Phase 1 master passes the self-check.

STYLE (prepend to every prompt, word for word):
"Stylized 3D render, soft clay-like materials, Pixar-inspired educational style, vibrant but clean colors, soft studio lighting, subtle ambient occlusion, high detail, crisp edges, no text, no watermark, no logos."

STYLE SCOPE: clay material and ambient occlusion apply ONLY to the subject, NEVER to the background.

BACKGROUND (append to every prompt, word for word):
"A single object floating in an empty void, centered, with 15% empty padding on all sides, fully visible and not cropped. Background is a flat, uniform, pure white #FFFFFF digital fill, identical in every pixel, like a blank canvas. No ground plane, no floor, no surface, no backdrop, no tile, no card, no panel, no frame, no border, no embossing, no texture, no gradient, no vignette, no cast shadow, no contact shadow, no reflection."

NEGATIVE PROMPT (use if supported):
"grid, multiple objects, tiles, cards, cushions, pillows, panels, borders, frames, embossed, debossed, carved into surface, relief, plaque, tray, table, floor, backdrop, drop shadow, contact shadow, gradient background, grey background, off-white background, paper texture, watermark, text."

COLOR RULES: starlight elements are warm gold (#FFC83D), hot elements are red-orange, cold elements are blue.

FILE FORMAT (STRICT): PNG only, 1:1, highest resolution. Never JPG or WEBP: compression adds noise to the white background and ruins background removal.

FILE NAMING (STRICT, NO EXCEPTIONS): rename every file to EXACTLY its ID plus ".png" (e.g. A1a_eye_front.png). Case-sensitive, underscores, no spaces. Do not keep tool default names and do not add suffixes like (1), _v2, _final, copy, dates or seeds. If you regenerate, overwrite the same filename. A file with the wrong name counts as NOT delivered, because the video code loads assets by exact filename.

GLOBAL RULES: ONE object per image. Never put multiple views in one image. Same seed for the whole batch if supported.

==================== PHASE 1: MASTER REFERENCES ====================
M1_eye_master: one freestanding 3D eyeball object, front view. Complete round eyeball with soft upper and lower eyelids and lashes attached, dark brown iris, glossy black pupil, bright glossy cornea highlight. Not part of a face, not embossed into any surface.
M2_astronaut_master: one cute stylized astronaut, three-quarter front view, standing neutral pose, white suit with gold reflective visor, small chest control panel, rounded proportions.
M3_icon_style_master: one chunky yellow pushpin icon, three-quarter view. This defines the clay material, edge softness and lighting for all icons.

==================== PHASE 2: VARIANTS ====================
For every variant: attach the listed master as the reference image (image-to-image / edit mode) and prepend:
"Keep the exact same design, proportions, colors, materials and lighting as the reference image. Change ONLY the following:"
then STYLE + variant description + BACKGROUND.

Eye variants (reference: M1_eye_master):
A1a_eye_front: identical to the master, clean final render.
A1b_eye_three_quarter: rotate the eyeball to a three-quarter view looking left.
A1c_eye_dilated: front view with the pupil noticeably dilated (larger black pupil, thinner iris ring).
A1d_eye_side: side profile showing the full spherical shape of the eyeball, cornea bulge visible.

Astronaut variants (reference: M2_astronaut_master):
A2a_astronaut_float_side: floating horizontally, side view, arms relaxed.
A2b_astronaut_look_left: standing, head and visor turned to look left.
A2c_astronaut_back: back view, backpack visible.
A2d_astronaut_wave: front view, right hand raised in a friendly wave.

Icon variants (reference: M3_icon_style_master, match material and lighting only):
A4a_icon_pushpin: identical to the master, clean final render.
A4b_icon_red_arrow: chunky curved red arrow pointing down-left.
A4c_icon_wind: swirling blue wind gust with three curled strokes.
A4d_icon_thermo_hot: red thermometer, liquid filled to the top.
A4e_icon_thermo_cold: blue thermometer, liquid low.
A4f_icon_magnifier: magnifying glass with a navy handle and light blue glass.

Single items (no master, but match the M3 material style):
A3_iss_window: one round ISS spacecraft window frame, metallic grey with bolts and a thick rim, seen straight on. The center hole shows the same pure white background.
A5_stargazer: one Indian teenager lying on a small rooftop mat looking up at the sky, side view, casual t-shirt, relaxed pose. The mat is the only prop, with no floor under it.

==================== SELF-CHECK (every image) ====================
Sample the four corners and the full border. Regenerate if any background pixel is not pure white #FFFFFF, if a shadow, surface, tile, card or texture is visible, if more than one object appears, if a Phase 2 variant drifts from its master, or if a watermark shows.

OUTPUT: 19 PNG files named exactly as the IDs above (3 masters + 16 finals). Return a table of filename, reference used, and final prompt.
```

---

## BATCH B Â· Glows Â· PNG Â· pure black BG

```
You are an image generation agent. Work in TWO PHASES: masters first, then variants. Generate everything in ONE session.

STYLE (prepend to every prompt, word for word):
"Stylized 3D render, soft clay-like materials, Pixar-inspired educational style, vibrant but clean colors, soft studio lighting, subtle ambient occlusion, high detail, crisp edges, no text, no watermark, no logos."

STYLE SCOPE: the style applies ONLY to the glowing element, NEVER to the background.

BACKGROUND (append to every prompt, word for word):
"A single glowing element, centered, on a pure solid black #000000 background, identical in every pixel. Nothing else in frame: no stars, no gradient, no vignette, no surface, no frame, no border."

NEGATIVE PROMPT (use if supported):
"grid, multiple objects, tiles, cards, panels, borders, frames, surface, floor, backdrop, gradient background, grey background, dark blue background, noise, extra stars, watermark, text."

COLOR RULES: starlight is warm white-gold (#FFC83D core fading to white), atmosphere glow is cyan-blue.

FILE FORMAT (STRICT): PNG only, 1:1, highest resolution (B2 is the only 16:9 exception). Never JPG or WEBP: compression adds noise to the black background and shows up as grey blotches under screen blend.

FILE NAMING (STRICT, NO EXCEPTIONS): rename every file to EXACTLY its ID plus ".png" (e.g. B1a_star_bright.png). Case-sensitive, underscores, no spaces. Do not keep tool default names and do not add suffixes like (1), _v2, _final, copy, dates or seeds. If you regenerate, overwrite the same filename. A file with the wrong name counts as NOT delivered.

GLOBAL RULES: ONE element per image, never a grid. Same seed for the whole batch if supported.

==================== PHASE 1: MASTER ====================
B1_star_master: one white-gold star glow, medium brightness, soft 4-point diffraction spikes, perfectly centered.

==================== PHASE 2: STAR VARIANTS ====================
Attach B1_star_master as the reference and prepend:
"Keep the exact same star shape, color and exact center position as the reference image. Change ONLY the following:"
B1a_star_bright: much brighter core, longer diffraction spikes, wider glow.
B1b_star_dim: smaller, fainter glow, short spikes.
B1c_star_pinpoint: tiny steady pinpoint, almost no spikes.

==================== SINGLE ELEMENTS ====================
B2_light_beam: one thin perfectly straight horizontal golden light beam with a soft outer glow and faint sparkle particles along it, spanning the full width of the frame. Aspect ratio 16:9.
B3_atmosphere_limb: a thin curved arc of glowing cyan-blue atmospheric haze, like Earth's limb seen from orbit. Only the glow, no planet.
B4a_flash_burst: one small white-gold lens flash burst.
B4b_highlight_ring: one soft circular glowing gold highlight ring, empty center.
B4c_normal_line: one thin vertical glowing white-gold line, soft glow, sharp core.
B4d_sparkle_twinkle: one four-point sparkle twinkle burst.
B5_space_dust: scattered tiny glowing dust particles and faint distant points of light, sparse, varied sizes (the only image allowed to have many small elements).

==================== SELF-CHECK (every image) ====================
Sample the four corners and the full border. Regenerate if any background pixel is not pure black #000000, if a gradient, vignette, frame or extra element is visible, if a star variant is not centered like the master, or if a watermark shows.

OUTPUT: 11 PNG files named exactly as the IDs above. Return a table of filename, reference used, and final prompt.
```

---

## BATCH C Â· Full frames Â· JPG Â· 9:16

```
You are an image generation agent. Generate every image below in ONE session so they share an identical look.

STYLE (prepend to every prompt, word for word):
"Stylized 3D render, soft clay-like materials, Pixar-inspired educational style, vibrant but clean colors, soft studio lighting, subtle ambient occlusion, high detail, crisp edges, no text, no watermark, no logos."

FRAMING (append to every prompt, word for word):
"Vertical 9:16 composition, 1080x1920, cinematic, full scene edge to edge."

COLOR RULES: night scenes use a deep navy base (#0B1330), starlight is warm gold (#FFC83D), atmosphere is cyan-blue.

CONSISTENCY RULES: all night skies use the same navy tone and star density. Leave the described empty areas clear, because elements get composited there later. Same seed for the whole batch if supported.

FILE FORMAT (STRICT): JPG only, quality 95, sRGB, exactly 1080x1920. Never PNG: no transparency is needed here and PNG only makes the files heavier.

FILE NAMING (STRICT, NO EXCEPTIONS): rename every file to EXACTLY its ID plus ".jpg" (e.g. C1_deep_space.jpg). Case-sensitive, underscores, no spaces. Do not keep tool default names and do not add suffixes like (1), _v2, _final, copy, dates or seeds. If you regenerate, overwrite the same filename. A file with the wrong name counts as NOT delivered.

IMAGES:
C1_deep_space: deep navy space with a faint purple-blue nebula, sparse starfield, a clear empty area in the center for a star.
C2_earth_orbit: Earth filling the bottom half of the frame seen from space, night side with warm city lights over India, glowing blue atmosphere edge, black space above.
C3_rooftop_sky: night sky over an Indian rooftop terrace, silhouettes of a water tank and railings at the bottom, dense starfield, calm and dark.
C4_night_ground: low-angle night scene, dark grassy horizon at the bottom, deep navy sky, empty center area for a large eye.
C5_iss_interior: inside the ISS looking out a round window, black space with one bright steady star, Earth's curve glowing blue at the window's bottom edge, soft cabin lights.

SELF-CHECK: regenerate if the size is not exactly 1080x1920, if any text or watermark appears, if the empty composite areas are cluttered, or if the navy tone differs between night scenes.

OUTPUT: 5 JPG files named exactly as the IDs above. Return a table of filename and final prompt.
```

---

## BATCH V Â· Veo 3 clips Â· MP4

Before running, composite `A1a_eye_front.png` onto `C4_night_ground.jpg` yourself and save it as `C4b_night_ground_eye.jpg`.

```
You are a video generation agent using Veo 3 image-to-video. Generate every clip below in ONE session.

STYLE (prepend to every prompt, word for word):
"Stylized 3D render, soft clay-like materials, Pixar-inspired educational style, vibrant but clean colors, soft studio lighting, subtle ambient occlusion, high detail, crisp edges, no text, no watermark, no logos."

RULES:
- Use the listed start frame image as the first frame.
- Vertical 9:16 if supported; otherwise 16:9 with the subject dead center for a vertical crop.
- 6 to 8 seconds, smooth camera motion, no cuts inside a clip.
- Audio is not needed (it will be muted).
- Never render text, labels or diagrams.

FILE FORMAT (STRICT): MP4 (H.264) only.

FILE NAMING (STRICT, NO EXCEPTIONS): rename every file to EXACTLY its ID plus ".mp4" (e.g. V1_star_to_earth.mp4). Case-sensitive, underscores, no spaces, no suffixes like (1), _v2, _final, copy, dates or seeds. Overwrite on regeneration. A file with the wrong name counts as NOT delivered.

CLIPS:
V1_star_to_earth (start frame: C1_deep_space.jpg): camera flies fast alongside a thin straight golden light beam shooting from a bright star through deep space, Earth grows larger ahead, the beam pierces the glowing blue atmosphere with a soft ripple, camera follows it inside.
V2_eye_flicker (start frame: C4b_night_ground_eye.jpg): slow push-in on a large stylized eye at night, a golden starlight beam wobbles and alternately hits the pupil (reflection flares bright) and misses it (reflection fades), rhythmic flicker, steady camera.
V3_iss_steady_star (start frame: C5_iss_interior.jpg): astronaut floats up to the ISS window and looks out, the single star outside stays perfectly still, gentle slow camera drift, calm mood.

OUTPUT: 3 MP4 files named exactly as the IDs above. Return a table of filename, start frame used, and final prompt.
```

---

## Built in Remotion (no prompts needed)
Shots 3, 4, 5 and 8: atmosphere bands, the bending beam (Snell's law), the wobble (noise), captions and the ATMOSPHERIC REFRACTION stamp. Planet tease: an on-screen text overlay in the last 2s, "Par planets twinkle kyun nahi karte? ðŸ¤” Part 2 mein", so the loop stays intact.