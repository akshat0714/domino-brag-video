# Brag Plan: Domino

## What is this app?
Domino lets hospitals find kidney-swap matches across hospitals without any patient file leaving its hospital. Each hospital runs its own agent on its own machine, answers a coordinator in categories only, and code does the matching.

## The angle
One family, one button, one network. The video opens on a single private family card (a willing donor whose kidney does not match), presses the product's one button, and pulls the camera back to show three hospitals answering from their own pods. The proof is the product's own end frame: 7 transplants, 0 patient records shared. Everything on screen is recreated from the real main screen and console, on the real basemap, with byte counts measured in a real LAN run.

## Hook (first 2-3 seconds)
A private family card on a quiet map of San Jose: patient Maria (blood type A), donor Elena, her sister (blood type B). The blood chips resolve to a red cross. Then the product's single button arrives: "Find a match for Maria".

## Key moments (the middle)
- The camera pulls back from one family to the whole network: three hospital pins, the coordinator hub, packets out and back.
- The agents panel ticking in all three pods at once: Received the form, Opened its own pod, Screened its pairs, Checked its rules, Replied over the network. Locked rows read "Stays inside Alder".
- "Names request refused by all 3 · 0 names shared".
- Routes draw on real roads, the counter goes 0 to 3, and the coordinator's own line appears: "They asked for one. The network found three."
- Real life: Riverbend holds ("R1 · first next round"), two legs turn red, the plan becomes a swap, counter 3 to 2.
- A gold courier leaves "YOU ARE HERE · STANFORD", the chain falls leg by leg, counter 2 to 7.

## Outro / punchline
The product's end frame, centred over the map with every route green: "7 transplants" then "0 patient records shared", under the Domino mark.

## User flow worth showing
Press "Find a match for Maria" → each hospital's agent works in its own pod and replies in categories only, refusing the names request → the network finds a loop, re-plans when real life breaks it, and a stranger's gift starts a chain → "7 transplants · 0 patient records shared".

## Tone
- Preset: polished
- Creative direction: quiet, logistics-grade product film. Light canvas, calm map, big numbers, few words.
- Interpretation: four scenes with long holds, slide and soft-focus transitions, one camera idea per scene, and restraint in sound. The product's own copy carries the message.

## Format: landscape — 1920x1080
## Duration: 24.4 seconds (set by the voiceover)

## Visual identity (from the project)
- Background: #f4f4f1 (map land), water #DCE7EF, highways #C3CAD5
- Accent: #2563eb (blue). Status colours from the product: green #16a34a, amber #d97706, red #dc2626, gold #ca8a04
- Text: #0f172a (ink), #64748b (muted)
- Display font: the product uses the system UI sans. The video uses Inter as the deterministic stand-in.
- Body font: same. Mono details in JetBrains Mono.
- Strongest visual element: the light map with three hospital pins and routes drawn on real roads, next to the big transplant counter.

## Honesty notes
- All people, hospitals and records are synthetic. The video says "synthetic data" in the top bar and the end card.
- Byte counts, the audit line and the mode badge come from the public event log of a real LAN run on 2026-09-29 (three hospitals connected, none simulated). The log was read without sending any command.
- The run in that log stops at step 6. The chain and the final count (2 to 7, end frame) come from the verified facts in docs/SPEC.md.
- The audit line is "audit: code checks only ✓" because no second-model key was set in that run.
- The hub is labelled "Coordinator". The product labels it "Flower SuperGrid · coordinator", but the measured run was LAN over WebSocket, so the video does not imply SuperGrid carried these packets. No sponsor strip is shown.
- Map attribution is on screen: © OpenStreetMap contributors · OpenFreeMap.

## Share copy (draft)
Introducing Domino: hospitals find kidney-swap matches across hospitals without any patient file leaving its hospital. 7 transplants, 0 patient records shared, on synthetic data.

## Audio direction
- Role: warm, steady bed under a calm narrator, with sparse professional accents.
- Music: happy-beats-business-moves-vol-12-by-ende-dot-app.mp3 (steady and clean, 110 BPM).
- Music treatment: starts at 0 with a short fade-in, sits at about 0.37 in the gaps, ducks to about 0.16 under each voiceover line, fades out over the last second. Final mix measures -18.3 LUFS integrated, peak -1.6 dBFS.
- Music cue guidance: bundled preset read (`assets/music/cues/happy-beats-business-moves-vol-12-by-ende-dot-app.music-cues.json`). Strong cues targeted: 8.74 s (replies land), 17.47 s (the gift leaves Stanford), 22.37 s (end line). Beat-grid windows: pod rows 6.56 to 8.74 s, chain legs 18.02 to 20.19 s.
- Audio-reactive treatment: subtle. Bass energy makes the status rings around the hospital pins and the hub halo breathe. No waveform or equalizer visuals.
- SFX posture: sparse, low-risk files, low volume.
- Audio-coupled moments: the button click, the replies landing, the counter reaching 3, the end line.
- Restraint rule: no sound may compete with the narrator. No accents on the pod rows or the chain legs; the beat carries them.

## Voiceover script
Voice: Kokoro `af_heart`, speed 0.95. One file per line, so each scene follows its own line. Lines start at 0.35, 5.30, 14.30 and 17.55 s.

1. "About a third of patients with a living donor can't use that donor's kidney." (4.29 s)
2. "Domino finds the swap across hospitals. Each agent answers from its own records." (5.27 s)
3. "When real life breaks the plan, it plans again." (2.77 s)
4. "Then a stranger gives, and a chain falls. Seven transplants. Zero patient records shared." (5.74 s)

The narration gives the reason and the stakes. The screen gives the evidence: the rows, the byte counts, the coordinator's own lines.

## Storyboard

### Scene 1 — One family — 0.0 to 4.95 s
The map sits close on San Jose with the Alder pin. A console-style family card: "A1", "Maria", blood chip A, then "donor Elena · sister", blood chip B, under the header "Families · private · this screen only". A step row resolves to a red cross: "Blood types · B cannot give to A". Then the dark button "Find a match for Maria" with its arrow.
Sequential/interaction: yes. Card, donor row, cross, button arrive one by one. A cursor glides in and presses the button at 4.91 s.
Audio intent: quiet opening, the narrator states the problem.
Audio-coupled idea: one soft click on the button press.
Music: steady bed, ducked under the line.
Transition mood: soft → Scene 2. The press starts the camera pull-back; the card lifts away as the network appears.

### Scene 2 — Private work — 4.95 to 11.0 s
Top bar: Domino mark, "LAN" badge, "3/3 hospitals online", "synthetic data". The map shows all three hospitals and the coordinator hub with dashed wires. Blue packets fly out, green packets fly back. On the right, the agents panel: three pods marked "own pod", five rows each, ticking together on the beat. Message pills under the hub: "→ Alder · screening form · 581 B", "← Harbor Point · names refused · 45 B". Then the callout at 9.29 s: "Names request refused by all 3" with "0 names shared".
Sequential/interaction: yes. Pins pop one by one. Rows resolve one beat apart (6.56, 7.09, 7.64, 8.19, 8.74 s). The rows are visible in their idle state from the start, so only the marks and byte counts arrive on the beat.
Audio intent: the bed opens up slightly between the two sentences.
Audio-coupled idea: replies land on the strong cue at 8.74 s with one soft drop.
Transition mood: clean slide → Scene 3. The camera pans, the panel leaves right, the counter card arrives left.

### Scene 3 — The match, then real life — 11.0 to 17.4 s
Left card: "This round", the big counter, the privacy line "0 patient records shared · 0 names shared · 8.4 KB sent". Three routes draw on real roads (11.46, 11.73, 12.02 s). The counter counts 0 to 3 and lands on the beat at 12.55 s with "Loop of 3 found" and "audit: code checks only ✓". The line "They asked for one. The network found three." holds for over two seconds with no narration. Then Riverbend turns amber with the chip "R1 · first next round", two legs turn red and fade, the plan becomes "Swap of 2", the counter drops to 2, and the line changes to "No consensus. Planning again without the held pair."
Sequential/interaction: yes. Three routes half a beat apart, then the re-plan in order (hold 14.73, broken legs 15.29, swap 16.38 s).
Audio intent: music alone for the match, then the narrator on the re-plan.
Audio-coupled idea: one warm soft impact when the counter reaches 3 at 12.55 s.
Transition mood: none, the scene continues → Scene 4 on the same card.

### Scene 4 — The stranger, the chain, the end frame — 17.4 to 24.4 s
A gold route and courier leave "YOU ARE HERE · STANFORD" for Alder at 17.47 s, under the coordinator's line "One stranger starts a chain of 5." The plan "Chain of 5 · 7 in total" is announced, then five chain legs draw with blue couriers, one per beat (18.02 to 20.19 s), and the counter climbs to 7. Every route turns green. The map softens and the end card arrives in the centre: the Domino mark, "Run complete", "7 transplants" at 21.84 s, "0 patient records shared" at 22.37 s, then "Synthetic data · Collaborative Agent Hackathon at Stanford, September 2026".
Sequential/interaction: yes. Gift, five legs, then two end lines.
Audio intent: the bed lifts into the chain, the narrator lands the two numbers, the music fades.
Audio-coupled idea: one soft bong on the end line at 22.37 s.
Transition mood: soft dissolve into the end card. Hold to the end.

**Music mood for this video:** steady, clean, quietly optimistic.
**Audio summary:** a calm narrator over a ducked, steady bed, with four quiet accents on the press, the replies, the match and the end line.
