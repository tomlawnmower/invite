# 🐾 Alice & Bob's Wedding Invitation

A responsive, mobile-first single-page wedding invitation web application designed for deployment on **GitHub Pages**. Features a light-blue theme, custom character artwork, dual-language support (**English** & **Traditional Chinese**), floating background decorations, and a complete RSVP form.

---

## ✨ Features

- 📜 **6 Scroll-Driven Sections**:
  1. **Save The Date (`#page2`)**: Feature photo, date badge, location overview, and floating background accents.
  2. **Invitation Prose (`#page3`)**: Formal invitation text in a glassmorphism card accompanied by a decorative envelope graphic (`images/bb_envelope.png`).
  3. **Venue & Schedule (`#page4`)**: Detailed event timeline, venue address, parking info, and centered header artwork (`images/nico_hat.png`).
  4. **Dress Code (`#page5`)**: Black-tie attire guidelines for ladies and gentlemen with flower crown artwork (`images/bb_flowercrown.png`).
  5. **FAQ (`#page6`)**: Collapsible accordion with header artwork (`images/bb_table.png` & `images/nico_peek.png`).
  6. **RSVP (`#page7`)**: Interactive RSVP form with guest count, dietary choices, special notes, and title artwork (`images/nico_delicious.png` & `images/nico_disgust.png`).

- 🌸 **Floating Background Decorations & Entrance Transitions**:
  - Over 40 floating background decorative elements (flowers, paws, hearts, stars, cakes, winking/running character art) distributed across all sections.
  - Automatically **fade in** as each section enters the viewport and **fade out** as you scroll away via `IntersectionObserver`.
  - Micro-animations powered by smooth CSS keyframes including floating (`anim-float`), swaying (`anim-sway`), pulsing (`anim-pulse`), and spinning (`anim-spin`).
  - Scaled down for mobile viewports (`< 576px`) to ensure optimal layout clarity and readability.

- 🌐 **Internationalization (i18n)**:
  - Toggle between **English** (`en`) and **Traditional Chinese** (`zh-TW`).
  - Automatically saves language preference in `localStorage`.

- 🐾 **Responsive & Elegant UI**:
  - Floating paw-print navigation dots with active section tracking using `IntersectionObserver`.
  - Soft light-blue palette, glassmorphism cards, micro-interactions, and fluid typography (*Playfair Display*, *Noto Serif TC*, *Quicksand*).

---

## 🛠️ Built With

- **HTML5 & CSS3**: Custom styles, CSS variables, glassmorphism cards, drop shadows, and keyframe animations.
- **JavaScript (ES6+)**: Custom i18n renderer, `IntersectionObserver`, and form handlers.
- **Bootstrap 4.5**: Grid layout, responsive utility classes, and accordion components.
- **Font Awesome 6**: Paw prints, map icons, and UI glyphs.
- **Google Fonts**: *Playfair Display*, *Noto Serif TC*, and *Quicksand*.

---

## 📁 Repository Structure

```text
├── index.html          # Main HTML markup containing all 6 page sections
├── styles.css          # Core design system, glassmorphism, animations & media queries
├── script.js            # i18n renderer, IntersectionObserver & form handlers
├── plan.txt            # Project roadmap & implementation notes
├── README.md           # Project documentation
└── images/             # Feature photo & decorative graphics
    ├── wedding.jpg             # Couple photo
    ├── bb_envelope.png         # Invitation envelope illustration
    ├── bb_flowercrown.png      # Flower crown illustration
    ├── bb_table.png            # Table illustration
    ├── nico_hat.png            # Character with hat illustration
    ├── nico_peek.png           # Peeking character illustration
    ├── nico_delicious.png      # Title illustration
    ├── nico_disgust.png        # Title illustration
    └── (flowers, hearts, paws, stars, cake & character accents)
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
