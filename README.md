# Netflix Clone – Landing Page

A responsive, front-end-only clone of the Netflix India landing/signup page — built with plain HTML and CSS (no frameworks, no build step).

## Features

- Cinematic hero section with dark vignette overlay, big headline and email signup form
- Sticky nav bar that blurs on scroll
- Four feature sections (Enjoy on your TV, Download to watch offline, Watch everywhere, Kids profiles) with autoplay preview videos and images
- Interactive FAQ accordion (click to expand/collapse, only one open at a time)
- Scroll-triggered reveal animation for each section
- Fully responsive layout (desktop → tablet → mobile)
- Accessible focus states on inputs and buttons

## Tech Stack

- HTML5
- CSS3 (custom properties, flexbox, media queries)
- Vanilla JavaScript (no libraries) — handles the FAQ accordion, nav scroll state, and scroll-reveal via `IntersectionObserver`
- Google Fonts: Poppins (body) + Bebas Neue (hero display headline)

## Project Structure

```
netflix-clone/
├── index.html          # Page markup
├── style.css            # All styling
├── README.md
└── images/
    ├── logo.svg          # Netflix wordmark
    ├── favicon.ico
    ├── bg-image.jpg       # Hero background
    ├── tv.png             # TV mockup (used twice, with video overlay)
    ├── mobile.jpg         # Phone mockup for offline downloads section
    ├── feature-4.png      # Kids profiles illustration
    ├── video-1.m4v        # Autoplay preview over tv.png (section 1)
    ├── video-2.m4v        # Autoplay preview over tv.png (section 3)
    ├── stranger.png       # Unused / extra asset
    ├── photo-vid2.png     # Unused / extra asset
    └── down-icon.png      # Unused / extra asset
```

## Running Locally

No build tools or dependencies needed.

1. Keep `index.html`, `style.css` and the `images/` folder together in one directory.
2. Open `index.html` directly in a browser, **or** serve it locally (recommended, since some browsers block local video/font loading over `file://`):

   ```bash
   # Python
   python3 -m http.server 8000

   # Node
   npx serve .
   ```
3. Visit `http://localhost:8000`.

## Notes / Known Limitations

- This is a **static front-end demo only** — the "Sign In", "Get Started" and footer links are not wired to any backend or routing.
- Email input has basic HTML5 `required`/`type="email"` validation only, no real submission handling.
- Autoplay videos are muted to comply with browser autoplay policies.
- Built for learning/portfolio purposes — not affiliated with or endorsed by Netflix.

## Possible Next Steps

- Wire up the email form to an actual sign-up flow (e.g. Express/Node backend)
- Add a real sign-in page and session handling
- Add a content carousel section (like the real Netflix homepage) with poster art
- Add dark/light or regional language toggle behind the "English" button
