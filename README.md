# HackSavvy-26 — Official Event Website

The official website for **HackSavvy-26**, a national-level 24-hour hackathon run by the **Mahatma Gandhi Institute of Technology (MGIT), Hyderabad** on **February 12–13, 2026**.

The site is the event's main information hub. It covers the hackathon themes, problem statements, schedule, guidelines, judging criteria, organizing team, highlights from past editions, and contact details, all on one responsive, animated page.

## Key Features

- **Animated hero section**: GSAP fade-in effects, plus scrolling tickers for event highlights (24 hours, ₹2.5L prize pool, mentors).
- **Five themes with collapsible problem statements**:
  - AI, Automation, Robotics & Drone Technology
  - Cybersecurity & Blockchain
  - IoT, VLSI & Embedded Systems
  - Sustainability & Environment
  - Open Innovation
- **Event schedule**: a two-day timeline.
- **Guidelines, FAQ and judging criteria**: the information participants need.
- **Leaders and organizing team**: an auto-scrolling team carousel with manual prev/next controls that resumes on its own.
- **Media & highlights**: an infinite auto-scrolling gallery of photos from HackSavvy-25 that pauses on hover.
- **Responsive design**: tuned for desktop, tablet and mobile.
- **No build step**: a pure static site that loads instantly and can be hosted anywhere.

## Tech Stack

| Layer      | Technology                                        |
| ---------- | ------------------------------------------------- |
| Markup     | HTML5 (semantic sections)                         |
| Styling    | CSS3 (custom styles, Flexbox, keyframe animations, media queries) |
| Scripting  | Vanilla JavaScript                                |
| Animation  | [GSAP 3](https://gsap.com/) (via CDN) + CSS keyframes |
| Icons      | Bootstrap Icons (via CDN)                         |
| Fonts      | Google Fonts: Orbitron, Inter                    |
| Hosting    | Any static host (Vercel / Netlify / GitHub Pages) |

## Project Structure

```
hacksavvy-26/
├── index.html          # Single-page site (markup, inline CSS & JS)
├── mgitlogo.png        # Hero logo
├── mgitwhitelogo.png   # Navbar logo
├── theme/              # Theme card images
├── leaders/            # Leadership photos
├── faculty/            # Faculty coordinator photos
├── student/            # Student coordinator photos
├── media/              # Highlights gallery from previous editions
└── README.md
```

## Running Locally

You don't need to install anything. The site is plain HTML, CSS and JS.

**Option 1: open it directly**

Open `index.html` in any modern browser.

**Option 2: serve it locally (recommended, closer to production)**

```bash
# Python 3
python -m http.server 8000

# or Node.js
npx serve .
```

Then visit <http://localhost:8000> (or the URL printed by `serve`).

> An internet connection is required for the CDN-hosted GSAP, Bootstrap Icons and Google Fonts.

## Configuration

- **Environment variables:** none. The site has no backend, API keys or secrets.
- **Content updates:** all content lives in `index.html`. To swap images, replace the files in their folders and keep the same filenames, or update the matching `src` paths.
- **Registration link:** the **Register** button in the header points to `#`. Change its `href` to the live registration form URL when it's ready.

## Deployment

The site is fully static, so it deploys to any static host with zero configuration:

- **Vercel**: import the repo, set the framework preset to *Other*, and leave the build command empty.
- **Netlify**: leave the build command empty and set the publish directory to `/`.
- **GitHub Pages**: deploy from the `main` branch, root folder.

## Credits

Organized by **MGIT, Hyderabad**.
Website developed by **Kriti Karunam**.
