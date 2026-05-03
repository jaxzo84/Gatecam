# 🏁 GateCam – RC Lap Timer with AprilTag detection

Made by Jonathan Wastring

Live at: `https://jaxzo84.github.io/gatecam`

---

## Setup – 3 steps

### 1. Create a GitHub repo named `gatecam`

### 2. Upload `index.html` to the repo

### 3. Enable GitHub Pages
Settings → Pages → Source: **Deploy from branch** → **main** → **/ (root)**

Done. Your timing system is live at `https://jaxzo84.github.io/gatecam`

---

## AprilTag detector

The app loads the AprilTag WASM detector automatically from unpkg CDN.
If you want it to work offline too, download these two files and put them in a `libs/` folder:

```
https://unpkg.com/apriltag-wasm@1.0.3/dist/apriltag_wasm.js
https://unpkg.com/apriltag-wasm@1.0.3/dist/apriltag_wasm.wasm
```

Your repo structure would then be:
```
index.html
libs/
  apriltag_wasm.js
  apriltag_wasm.wasm
```

---

## Print cards

- Go to the **Print Cards** tab
- Enter a range (e.g. 1–30)
- Click **Print** → browser print dialog opens
- Cards are 4 per A4 sheet
- Use **matt lamination** – glossy reflects light and breaks detection
- Cards are reusable across event days

## Camera setup

- Mount camera in the gate, pointing straight down
- Adjust gate height so the car roof (and tag) fills a reasonable portion of the frame
- 720p 60fps recommended
- A USB webcam on a simple bracket works well

## Workflow

**Before the event:**
- Print and laminate a batch of cards (e.g. #1–60)
- No names needed – cards are reusable

**Race day morning:**
- Drivers tab: assign tag numbers to drivers for today
- Give each driver their card
- At end of day: hit "Clear all tag assignments"

**Per heat:**
- Race Setup: tick the drivers in this heat, set laps/debounce
- Live Race: start camera, start race
- Results: export to text file
