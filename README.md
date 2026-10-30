# Birthday Escape Room

A personalised multi-stage birthday experience — a scuba diving themed escape room delivered entirely via a single URL. 

---

## Concept

The player progresses through a series of real-world and digital puzzle stages over several days, culminating in an underwater-themed digital escape room. Each stage unlocks the next via an admin panel.

---

## Scenes

| File | Description |
|---|---|
| `index.html` | Entry point — "Find the treasure" landing screen |
| `Escape Room Day.html` | Daytime beach scene — animated sky, sun, ocean, cliffs, seagulls |
| `Escape Room Night.html` | Night beach scene — stars, moon reflection, torches, bioluminescent cave glow |
| `Cave Interior.html` | Underwater cave chamber — stalactites, water caustics, stone platform, floor hatch |
| `admin.html` | Supabase-backed admin panel to approve, fail, or reset puzzle stages |

---

## How it works

Each scene contains a 4-digit combination lock. The player examines the environment for clues (tide charts, sea patterns) and enters the code via an on-screen keypad or physical keyboard.

- Correct code → padlock animates open, door/hatch swings open, success screen appears
- Wrong code → digit boxes shake and flash red
- Keyboard support: number keys, Backspace, Enter, Escape

Stage progression is managed via the admin panel — the host approves or fails each real-world task to unlock the next digital stage.

---

## Tech stack

Pure vanilla HTML, CSS, and JavaScript — no frameworks, no build step. Open any `.html` file directly in a browser.

- SVG for all scene artwork and animations
- CSS animations for waves, torch flames, sparkles, sunlight shafts, water caustics
- Supabase (admin panel only) for multi-stage progress tracking

---

## Running it

No install required. Open `index.html` in a browser to start, or open any individual scene file directly.

For the admin panel (`admin.html`), a Supabase project is required with the matching environment config.

---

## Theme

Nautical and underwater — a treasure hunt that moves from sunlit beach through nightfall into a submerged cave. Ocean blues, sandy tans, and cave grays with dynamic lighting throughout.
