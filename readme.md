# NOMAGEV HUB: The Retro Mainframe

This is the central command center for all **@nomagev** projects. It is built as a single-page application (SPA) using **NES.css** to mimic an 8-bit gaming console interface.

---

##  Project Architecture (The "Code Lesson")

This repository serves as a live example of **Backlog Item #8: Code Simplification**. Instead of heavy frameworks, it uses vanilla JavaScript and CSS to achieve high-fidelity retro effects.

### 1. The Boot Sequence (`runBootSequence`)
The "BIOS" screen at the start uses an `async` loop to simulate system initialization.
* **The Logic:** It iterates through an array of strings, creating a new `div` for each line.
* **The "Human" Feel:** We use `Math.random()` to vary the typing speed, making it look like a real 1980s processor is processing data.

### 2. The CRT Glitch Effect
The glitch is a combination of **CSS Keyframes** and a **JavaScript Reflow**.
* **CSS:** Uses `text-shadow` with red/blue offsets to create an "RGB Split" (Chromatic Aberration).
* **JS:** The `randomGlitch()` function uses `void el.offsetWidth;`. This is a "hack" that forces the browser to recalculate the element's position, allowing us to restart a CSS animation instantly on command.

### 3. Dynamic Level Select (GitHub API)
To fulfill the automation requirement, the site fetches repository data directly from the GitHub API.
* **Sorting:** It sorts by `pushed_at`, so your most recently updated project always appears as "LEVEL 1."
* **Status:** It dynamically checks for descriptions and URLs, meaning the hub updates itself every time a new repository is created.

---

## 📂 File Structure
* `index.html`: The core logic, CSS animations, and UI structure.
* `blim_art.txt`: Standalone ASCII art file (Isolated per **Backlog Item #5**).
* `.github/workflows/`: Automation scripts to keep the GitHub Pages deployment fresh.

---

## 📜 Licensing
This project is licensed under the **GPL 2.0 License**. 

> "The freedom to share and change all versions of a program—to make sure it remains free software for all its users."

---

## 🚀 Backlog Progress
- [x] Markdown Support (UI Integration)
- [x] Blim.py ASCII Art Isolation
- [x] GPL 2.0 License Implementation
- [x] Automated Repository Listing
- [ ] Code Simplification (Phase 2)
- [ ] Full Human-Readable Code Lesson