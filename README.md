# 🧠 Memory Experiment — Avila College

**How does music affect short-term memory?**

A browser-based psychology experiment that tests the effect of background music on short-term word recall in female students aged 17–18. Built as a single HTML file — no server, no installation, no dependencies to manage. Open the file in a browser and start collecting data.

> **Live demo:** [https://sophiabutton.github.io/memory-experiment/](https://sophiabutton.github.io/memory-experiment/)

---

## About the Experiment

Participants memorise a list of 10 words under three audio conditions, then try to recall as many as possible. The experiment measures how each condition affects recall accuracy.

| Condition | Description |
|-----------|-------------|
| 🔇 Silence | No background audio |
| 🎵 Instrumental | Background music without lyrics |
| 🎤 Lyrics | Background music with sung lyrics |

Conditions are always tested in the same order (Silence → Instrumental → Lyrics) to maintain consistency across participants. Word lists are **randomly assigned** to conditions for each participant to control for difficulty differences between lists.

---

## How It Works

Each participant goes through the following flow:

```
Welcome → Setup → [Memorise → Recall → Break] × 3 → Results
```

1. **Setup** — Enter a participant name or ID.
2. **Memorise** — 10 words are displayed on screen for **60 seconds**. The experimenter manages audio playback externally via a speaker.
3. **Recall** — Words disappear and the participant types every word they remember (no time limit).
4. **Break** — A short rest between conditions with instructions for the next round.
5. **Results** — Scores are shown with a word-by-word breakdown.

After each participant finishes, click **Next Participant** to begin the next session. All data accumulates in memory across participants until exported.

---

## Data Export

All participant data is stored in the browser session and can be exported at any time from the Results screen.

**Download Excel** — Exports an `.xlsx` file with two sheets:

| Sheet | Contents |
|-------|----------|
| Raw Data | One row per word per participant — includes condition, target word, what was entered, and whether it was correctly recalled |
| Summary | One row per participant per condition — includes total score and percentage |

**View All Data** — Opens an in-app modal showing the raw data in CSV format for quick inspection.

> ⚠️ **Important:** Data is stored in browser memory only. If you close or refresh the page, all unsaved data is lost. Export your data before closing the browser.

---

## Word Lists

Three balanced 10-word lists of academic vocabulary:

| List 1 | List 2 | List 3 |
|--------|--------|--------|
| Expand | Establish | Analyse |
| Method | Increase | Achieve |
| Benefit | Process | Assist |
| Evaluate | Approach | Design |
| Structure | Approximate | Select |
| Impact | Function | Identify |
| Concept | Respond | Compose |
| Maintain | Interpret | Revise |
| Develop | Sequence | Integrate |
| Observe | Validate | Justify |

Lists are shuffled and randomly assigned to conditions for each participant.

---

## Deployment on GitHub Pages

1. **Create a repository** on GitHub (e.g. `memory-experiment`).
2. **Upload** `memory-experiment.html` and rename it to `index.html`.
3. Go to **Settings → Pages** and set the source to the `main` branch.
4. Your experiment will be live at `https://yourusername.github.io/memory-experiment/`.

No build step or server required — it's a single static HTML file.

---

## Running Locally

Just open the file in any modern browser:

```bash
# macOS
open memory-experiment.html

# Windows
start memory-experiment.html

# Linux
xdg-open memory-experiment.html
```

Or double-click the file in your file manager.

---

## Technical Details

- **Single-file architecture** — all HTML, CSS, and JavaScript in one file
- **No backend** — runs entirely in the browser
- **Excel export** via [SheetJS (xlsx.js)](https://sheetjs.com/) loaded from CDN
- **Fonts** — DM Serif Display and DM Mono from Google Fonts
- **Fullscreen mode** — toggle button in the top-right corner for distraction-free testing
- **Responsive** — works on tablets and desktops (not optimised for phones)

---

## Requirements

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- An internet connection on first load (for Google Fonts and SheetJS CDN)
- External speaker or headphones for playing music during instrumental and lyrics conditions

---

## Licence

This project was created for educational and research purposes at Avila College.
