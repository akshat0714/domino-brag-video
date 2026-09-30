# Hyperframes Composition Brief: Domino

## Objective
Create a short launch-style brag video for Domino.

## Output
- Composition directory: `brag-output/composition/`
- Rendered video: `brag-output/brag.mp4`
- Format: landscape — 1920x1080
- Duration: 24.4 seconds

## Source Material
- Project root: `domino-map/`
- Primary files read: `README.md`, `docs/SPEC.md`, `src/index.css`, `src/screens/main/main.css`, `src/screens/main/parts.tsx`, `src/screens/main/state.ts`, `src/screens/main/MainScreen.tsx`, `src/screens/console/ConsoleScreen.tsx`, `src/screens/console/console.css`, `src/map/scene.ts`, `src/map/scenes.ts`, `src/map/places.ts`, `src/map/basemap.ts`, `public/routes.json`, `data/domino-data.json`, `shared/protocol.ts`
- Product name: Domino
- Tagline / strongest claim: "7 transplants · 0 patient records shared"
- Key UI or visual moment to recreate: the main screen's map with three hospital pins and road routes, the counter card, and the agents panel with its "own pod" rows
- Copy that must appear verbatim:
  - Find a match for Maria
  - Received the form / Opened its own pod / Screened its pairs / Checked its rules / Replied over the network
  - Names request refused by all 3
  - They asked for one. The network found three.
  - No consensus. Planning again without the held pair.
  - 7 transplants / 0 patient records shared

## Creative Direction
- Tone preset: polished
- Creative direction: quiet, logistics-grade product film
- Interpretation: four scenes, long holds, slide and soft-focus transitions, sparse sound
- Angle: one family, one button, one network. Open on a private family card, press the product's one button, pull back to three hospitals answering from their own pods, and end on the product's own end frame.
- Hook: the family card whose blood chips resolve to a red cross, then the button "Find a match for Maria"
- Outro / punchline: "7 transplants" then "0 patient records shared" under the Domino mark
- Avoid:
  - Generic SaaS language
  - Abstract filler visuals
  - Unrelated visual redesign
  - Any claim that packets travelled over Flower SuperGrid, or any sponsor strip

## Visual Identity
- Background: #f4f4f1
- Text: #0f172a, muted #64748b
- Accent: #2563eb, with the product's status colours (green #16a34a, amber #d97706, red #dc2626, gold #ca8a04)
- Display font: Inter (bundled stand-in for the product's system UI sans)
- Body font: Inter, with JetBrains Mono for pair ids
- Visual references from the project: the Positron basemap as tuned by `basemap.ts`, the pin and label card from `index.css`, the card, chip, mark and result styles from `main.css`, the family card and blood chips from `console.css`

## Storyboard
Use the storyboard in `brag-output/brag-plan.md` as the creative contract.

Scene summary:
1. One family — 0.0 to 4.95 s — family card, red cross on blood types, the button, a cursor press
2. Private work — 4.95 to 11.0 s — three hospitals, packets, the agents panel ticking, names refused
3. The match, then real life — 11.0 to 17.4 s — routes draw, counter 0 to 3, the hold, counter 3 to 2
4. The stranger, the chain, the end frame — 17.4 to 24.4 s — gold courier, five legs, counter to 7, end card

## Audio
- Audio role: warm bed under a calm narrator, sparse professional accents
- Audio arc: quiet opening, steady middle, a lift into the chain, fade on the end card
- Music: `happy-beats-business-moves-vol-12-by-ende-dot-app.mp3`
- Music treatment: about 0.37 in the gaps, ducked to about 0.16 under each narration line through a volume lane, fade out over the last second; narration at 1.3
- Music cue guidance: bundled preset `assets/music/cues/happy-beats-business-moves-vol-12-by-ende-dot-app.music-cues.json`; strong cues 8.74, 17.47 and 22.37 s; beat-grid windows 6.56 to 8.74 s and 18.02 to 20.19 s
- Audio-reactive treatment: subtle; bass energy drives the status rings around the pins and the hub halo
- Audio-coupled moments:
  - Scene 1, 4.91 s — simulated button press
  - Scene 2, 8.74 s — replies land
  - Scene 3, 12.55 s — counter reaches 3
  - Scene 4, 22.37 s — end line
- SFX selection guidance: low high-frequency-risk files only, low volume, never over a narrated word where it can be avoided
- SFX analysis guidance: `assets/sfx/sfx-analysis.md` in the brag skill
- Exact SFX choice: Hyperframes chooses filenames, timestamps, density and volume from the implemented animation.
- Audio files: copied into `brag-output/composition/assets/`
- Voiceover: Kokoro `af_heart`, four files in `assets/vo/`, one per line; scene lengths follow the measured line lengths

## Hyperframes Instructions
Load the composition-building Hyperframes domain skills — `hyperframes-core`, `hyperframes-animation`, `hyperframes-creative`, `hyperframes-keyframes`, and `hyperframes-cli`. /brag is its own workflow: do not enter the `hyperframes` entry-point intent interview and do not route into its generic promo / launch-video workflow. Prefer native Hyperframes conventions over anything in `/brag`.

Requirements:
- Show at least one real UI, copy, or visual element from the source project.
- Keep all text readable in the final render.
- Keep the video within 15-25 seconds.
- Include the planned music, SFX and voiceover layer.
- Treat `/brag` audio notes as guidance, not a fixed cue sheet.
- Use local assets for audio, the map image and GSAP.
- Run `hyperframes check` before render — it is brag's single gate.
