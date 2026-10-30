# Free Body Diagram Practicer

A whole-class free body diagram practice tool for Unit 3: Newton's Laws (Chem/Phys). Put it on the projector, read the prompt, have students draw the FBD on their whiteboards, then click to reveal the answer. It runs in any browser with no install and no accounts.

## What is in it

29 prompts that get harder as you go:

| Level | Prompts | Covers |
|---|---|---|
| 1. Flat ground | 7 | Objects at rest, constant velocity vs. speeding up, sliding to a stop, frictionless motion, hanging objects, tension |
| 2. Through the air | 8 | Projectiles with only F<sub>g</sub> (going up, at the top, angled launch, rolling off a table), then air resistance (skydiver speeding up, terminal velocity, parachute, ball thrown up with air) |
| 3. Magnitudes & F<sub>net</sub> | 8 | Forces given in newtons. Find F<sub>net</sub> (size and direction), including two forces in the same direction, missing forces at constant velocity, and F<sub>N</sub> ≠ F<sub>g</sub> |
| 4. Ramps | 6 | Drawing only: F<sub>g</sub> straight down, F<sub>N</sub> perpendicular to the ramp, friction along the ramp, and a gentle vs. steep comparison |

Labels match the Unit 3 slides: F<sub>N</sub>, F<sub>app</sub>, F<sub>g</sub>, F<sub>f</sub>, plus F<sub>T</sub> (tension) and F<sub>air</sub> (air resistance). F<sub>net</sub> is written as "0 N; No Direction" or "20 N to the right".

Each answer shows the FBD (arrows draw in one at a time), Balanced or Unbalanced, F<sub>net</sub>, a short "why", and a "Watch for" line with the common mistake. The FBD is sized to fill the answer panel so it reads well on a projector. On wide, short screens the text sits beside the diagram; on taller screens it sits underneath.

## Using it in class

- **Reveal:** click the answer panel, the Reveal button, or press Space.
- **Keyboard or clicker:** → (or Page Down) reveals the answer, press again for the next question. ← (or Page Up) goes back.
- **Short on time?** Click **Skip this one** on any question. Next and Back pass over skipped questions, and the number buttons show them crossed out. **Clear skips** brings them all back.
- **Jump around:** click a level tab or a question number.
- **FBD Rules:** opens the steps from the slides and a key of all six forces.
- **Full screen:** hides the browser bars and the keyboard hint so the answer diagram gets as much room as possible.

The page remembers which question you were on and which ones you skipped, in that browser only.

## Put it on GitHub Pages

1. Sign in at github.com and click **New repository**. Name it something like `fbd-practicer`.
2. Set the repository to **Public**. Free GitHub Pages only works on public repositories.
3. Click **uploading an existing file**. Open the folder, select **both files inside it** (index.html and this README) and drag them in. Upload the files themselves, not the folder that contains them.
4. Click **Commit changes**.
5. Go to **Settings > Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, Branch to **main** and folder to **/ (root)**, then click **Save**.
6. Wait a minute or two and refresh. The link appears at the top of the Pages screen, like `https://madisonwebb01.github.io/fbd-practicer/`.

**Troubleshooting:** if you get a 404 page, index.html was uploaded inside a subfolder. Make sure index.html sits at the top level of the repository, not inside another folder.

## Edit or add questions

All questions live in index.html in the list that starts with `var Q = [`. Each question looks like this:

```js
{lv:0, p:"A book is resting on a table.", t:"",
 sc:{t:"floor", o:"book", surf:"table"},
 d:[{f:[F("g",270,.62),F("N",90,.62)]}],
 net:{bal:true},
 why:["First bullet.","Second bullet."],
 watch:"The common mistake."},
```

- `lv`: level (0 = Flat ground, 1 = Through the air, 2 = Magnitudes, 3 = Ramps)
- `p`: the prompt. `t`: an optional purple line under it (leave `""` for none)
- `sc`: the scene sketch (`floor`, `air`, `hang`, `rope`, `ramp`)
- `d`: the answer diagram. `F("g",270,.62)` means F<sub>g</sub>, pointing 270° (down), arrow length 0.62. Directions: 0 right, 90 up, 180 left, 270 down. Add `{v:"50 N"}` to show a magnitude.
- `net`: `{bal:true}` for balanced, or `{bal:false, val:"20 N", dir:"to the right"}`

Created using Claude by Madison Webb, 2026.
Anthropic. (2026). *Claude* [large language model]. https://claude.ai
