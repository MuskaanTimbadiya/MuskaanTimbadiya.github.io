# Muskaan Timbadiya — Senior Quality Engineer Portfolio

This is a premium, professional, and interactive portfolio website designed to showcase the expertise of Muskaan Timbadiya as a Senior Quality Engineer, specializing in test automation frameworks, cloud-native testing, and quality engineering culture.

## Chosen Vertical: Quality Engineering & Test Automation Architecture

The design, branding, and interactive components of this website are tailored to appeal to tech recruiters and engineering managers looking for senior test automation leaders. Rather than using generic web templates, this site incorporates:
- **Automation Aesthetics:** Interactive components themed around software verification, metrics, and CI/CD pipelines.
- **QE Control Center:** An interactive dashboard in the hero section displaying circular progress rings for key system indicators (uptime, pass rate, coverage) alongside a real-time CI/CD pipeline visualizer.
- **Interactive QA Terminal:** A live simulated testing terminal in the contact section that showcases standard automated test flows (Playwright migrations, REST Assured API tests, Maven setups, and multi-stage builds) verifying system performance in real-time.
- **Confidence Metrics:** Highlighting statistics like pass rate, tests optimized, speed gains, and uptime, which are critical KPIs for senior QA leaders, with animated count-up effects on scroll.

## Approach & Logic

### 1. Unified Theming & Glassmorphism
We introduced a cohesive CSS Variable-driven theme system with a smooth toggle between two premium states:
- **Light Theme (Deep Navy & Silver):** Clean, corporate, and highly professional layout prioritizing readability and clear typography using deep royal blues (`#0f2e5c`) and emerald highlights.
- **Dark Theme (Obsidian & Glowing Indigo):** A developer-focused high-tech layout with glassmorphic cards (`backdrop-filter: blur()`), subtle border glows, and glowing teal/indigo gradients.

### 2. High-Fidelity Micro-Animations
To make the site feel responsive and alive:
- **Animated Count-up Stats:** Scroll-triggered counting animations for numerical metrics (e.g. from `0` to `5+`, `80%+`, `900+`, `30%`, `99.9%`) when they enter the viewport.
- **Ambient Glowing Spotlight:** A dynamic radial gradient background follows the user's cursor across the hero grid to create depth.
- **Floating Decorative Blobs:** Ambient soft-colored background circles that slowly drift using CSS keyframes, giving a modern UI/UX feel.
- **Magnetic Custom Cursor:** A lightweight custom cursor featuring an inner dot and a trailing outer ring that expands and snaps to interactive elements (buttons, links, cards). It auto-disables on touch screens and handles screen-leave mouse boundaries safely.
- **Smooth Hover States:** Custom lifts, shadow expands, and border-glows on all experience, achievement, and repository cards.

### 3. Simplicity & Performance
- Built using vanilla HTML, CSS, and modern ES6 JavaScript.
- Avoided large external frameworks to keep the repository extremely lightweight (well under the 10 MB limit).
- Utilized CSS transition properties and hardware-accelerated animations for buttery smooth 60fps rendering.

## How the Solution Works

### Key Structure
- **[index.html](file:///Users/muskaantimbadiya/Downloads/MuskaanTimbadiya.github.io/index.html):** The single entry point containing the structured content, styles, and behavioral scripts.
- **Theme Manager:** Checks local storage for the user's theme preference and falls back to system preferences (`prefers-color-scheme`). Toggles classes on the `<html>` or `<body>` element.
- **QE Control Center:** Toggles between `Overview` (SVG metrics, counters) and `CI/CD Pipeline` (timeline stepper) tabs dynamically, linking the terminal logs directly to the visual status icons.
- **Terminal Simulation Engine:** A JavaScript-driven loop that parses clicked or typed commands (`help`, `clear`, `pipeline`, `metrics`, `skills`) and animates responses. When `pipeline` is triggered, it outputs a simulated step-by-step Quality Assurance execution run.
- **Intersection Observer:** Triggers stagger reveal animations on sections, cards, and timeline entries as the user scrolls them into view.

## Assumptions Made
1. **Device Support:** Custom cursors and mouse-tracking spotlights require hover/mouse states. We assume touch/mobile devices should bypass cursor rendering and follow normal touch gestures to avoid layout bugs.
2. **GitHub API Availability:** The profile-data fetch utilizes raw data from a separate repository fallback. The site is designed with elegant skeleton loaders to display temporary placeholder content while the API request completes, preventing sudden layout shifts.
3. **No Build Step:** Since this is hosted directly on GitHub Pages, we assume a static asset structure with no Node build steps or transpilation is preferred, making deployment instant.
