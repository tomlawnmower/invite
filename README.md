# 🐾 Alice & Bob's Wedding Invitation

A responsive, mobile-first single-page wedding invitation web application designed for deployment on **GitHub Pages**. Features a light-blue theme, custom character artwork, interactive video scrubbing on scroll, dual-language support (**English** & **Traditional Chinese**), dynamic scroll-driven floating background decorations, and a complete RSVP form.

---

## ✨ Features

- 📜 **7 Scroll-Driven Sections**:
  1. **Envelope (`#page1`)**: Interactive intro video scrubbing on scroll (`video/intro_scrub.mp4`).
  2. **Save The Date (`#page2`)**: Feature photo, date badge, location overview, and floating background accents.
  3. **Invitation Prose (`#page3`)**: Formal invitation text in a glassmorphism card accompanied by a decorative envelope graphic (`images/bb_envelope.png`).
  4. **Venue & Schedule (`#page4`)**: Detailed event timeline, venue address, parking info, and header artwork (`images/nico_hat.png`).
  5. **Dress Code (`#page5`)**: Black-tie attire guidelines for ladies and gentlemen with flower crown artwork (`images/bb_flowercrown.png`).
  6. **FAQ (`#page6`)**: Collapsible accordion with header artwork (`images/bb_table.png` & `images/nico_peek.png`).
  7. **RSVP (`#page7`)**: Interactive RSVP form with guest count, dietary choices, special notes, and title artwork (`images/nico_delicious.png` & `images/nico_disgust.png`).

- 🌸 **Dynamic Scroll-Driven Background Decorations**:
  - Over 40 floating background decorative elements (flowers, paws, hearts, stars, cakes, winking/running character art) distributed across pages 2–7.
  - Automatically **fade in** as each section enters the viewport and **fade out** as you scroll away via `IntersectionObserver`.
  - Micro-animations including floating (`anim-float`), swaying (`anim-sway`), pulsing (`anim-pulse`), and spinning (`anim-spin`).
  - Scaled down for mobile viewports (`< 576px`) to preserve clarity and readability.

- 🌐 **Internationalization (i18n)**:
  - Toggle between **English** (`en`) and **Traditional Chinese** (`zh-TW`).
  - Automatically saves language preference in `localStorage`.

- 🎬 **Virtual Scroll Video Scrubbing**:
  - Scroll-driven frame scrubbing mapped smoothly to a virtual pixel budget.
  - Keyframe-optimized video (`video/intro_scrub.mp4`) with `fastSeek()` for instantaneous, 1:1 scroll scrubbing across trackpads, mice, and touch devices.

- 🐾 **Responsive & Elegant UI**:
  - Floating paw-print navigation dots with active section tracking using `IntersectionObserver`.
  - Soft light-blue palette, glassmorphism cards, micro-interactions, and fluid typography (*Playfair Display*, *Noto Serif TC*, *Quicksand*).

---

## 🛠️ Built With

- **HTML5 & CSS3**: Custom styles, CSS variables, glassmorphism cards, drop shadows, and keyframe animations.
- **JavaScript (ES6+)**: Custom i18n renderer, virtual scroll accumulator, and `IntersectionObserver`.
- **Bootstrap 4.5**: Grid layout, responsive utility classes, and accordion components.
- **Font Awesome 6**: Paw prints, map icons, and UI glyphs.
- **Google Fonts**: *Playfair Display*, *Noto Serif TC*, and *Quicksand*.

---

## 📁 Repository Structure

```text
├── index.html          # Main HTML markup containing all 7 page sections
├── styles.css          # Core design system, glassmorphism, animations & media queries
├── script.js            # i18n renderer, video scrub engine, IntersectionObserver & form handlers
├── plan.txt            # Initial project plan
├── README.md           # Project documentation
├── images/             # Feature photo & decorative graphics
│   ├── wedding.jpg             # Couple photo
│   ├── bb_envelope.png         # Invitation envelope illustration
│   ├── bb_flowercrown.png      # Flower crown illustration
│   ├── bb_table.png            # Table illustration
│   ├── nico_hat.png            # Character with hat illustration
│   ├── nico_peek.png           # Peeking character illustration
│   ├── nico_delicious.png      # Title illustration
│   ├── nico_disgust.png        # Title illustration
│   └── (flowers, hearts, paws, stars, cake & character accents)
└── video/
    ├── intro.mp4       # Original intro video
    └── intro_scrub.mp4 # Keyframe-optimized video (all keyframes) for smooth scroll scrubbing
```

---

## 🚀 Local Setup & Deployment

### Running Locally
This is a static web application with no build steps required. Open `index.html` directly in your browser or run a simple local HTTP server:

```bash
# Using Python
python3 -m http.server 8000

# Or using Node npx
npx serve .
```

Then open `http://localhost:8000` in your web browser.

### Deploying to GitHub Pages
1. Push your changes to your GitHub repository:
   ```bash
   git add .
   git commit -m "Update wedding invitation website"
   git push origin main
   ```
2. Go to **Settings > Pages** in your GitHub repository.
3. Select `main` branch as the source and root `/` folder, then click **Save**.
4. Your website will be published live at `https://<username>.github.io/<repo-name>/`.
