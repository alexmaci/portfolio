# Alejandro Vicente Macian — Portfolio

Personal portfolio website for Alejandro Vicente Macian, a Senior Java Backend Engineer specializing in Java, Spring Boot, microservices, Apache Kafka, cloud development and enterprise integrations.

The site is intentionally lightweight: plain HTML, CSS and JavaScript with no build step, framework or runtime dependency.

## Preview locally

From the project directory, run:

```bash
python3 -m http.server 4173
```

Then open [http://localhost:4173](http://localhost:4173).

## Project structure

```text
.
├── index.html             # Complete portfolio markup and content
├── styles.css             # Responsive visual design and layout
├── script.js              # Mobile navigation and small interactions
├── Portrait.png           # Original portrait asset
└── assets/
    ├── portrait.webp      # Optimized portrait used by the hero
    ├── origin-logo.svg     # Origin Creators logo
    └── favicon.svg        # Site favicon
```

## Website sections

- Hero and professional introduction
- Featured Gosbi ecommerce and ERP integration case study
- Orion Clinic / healthcare professional highlight
- Complete professional experience timeline
- Technical expertise and full CV technology stack
- Origin Creators, presented as a secondary independent initiative
- Education and languages
- Contact section with email and LinkedIn links

## Content sources

Professional content is based on the supplied CV and LinkedIn About text. The website is written entirely in English and does not include internationalization or a language switcher.

The Gosbi case study describes Alejandro's backend integration work for SII Group Spain. It clearly distinguishes that work from Gosbi's ecommerce frontend and avoids inventing confidential metrics or architecture details.

## Image optimization

The hero uses `assets/portrait.webp`, generated from the original `Portrait.png` to reduce page weight. If the original portrait changes, regenerate the WebP with Pillow:

```bash
python3 - <<'PY'
from PIL import Image

image = Image.open("Portrait.png").convert("RGB")
image.thumbnail((1000, 1000), Image.Resampling.LANCZOS)
image.save("assets/portrait.webp", "WEBP", quality=84, method=6)
PY
```

## Design and accessibility

- Responsive layouts for desktop, tablet and mobile screens
- Dark, technical visual direction with lime accent color
- Keyboard-visible focus states and a skip link
- Semantic headings, landmarks and descriptive image text
- Mobile navigation with `aria-expanded` state and Escape-key support
- Reduced-motion support through `prefers-reduced-motion`
- External links use `target="_blank"` with `rel="noopener noreferrer"`
- SEO title, description, Open Graph metadata and semantic page structure

The local page was checked with Lighthouse for accessibility, best practices and SEO.

## Deployment

Because this is a static site, it can be deployed directly to GitHub Pages, Netlify, Vercel, Cloudflare Pages or any static web server. No build command is required. Publish the repository root as the site directory.

## Maintenance notes

- Keep all visible content in English.
- Update professional details from the CV or LinkedIn profile rather than adding unsupported claims.
- Preserve the distinction between Gosbi's client website and Alejandro's backend integration contribution.
- Keep Origin Creators secondary to the engineering career.
- If the portrait is replaced, keep an optimized local WebP version for performance.
