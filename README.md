# EliteHomes

EliteHomes is a static, single-page real-estate landing page built around a polished property-discovery experience. The page presents featured listings, service categories, client testimonials, FAQs, and contact information in a responsive layout.

> This repository is a front-end visual/demo site. The listing search, contact form, social links, and action buttons are currently UI-only: no backend, database, listing API, or form submission endpoint is included.

## Highlights

- Hero section with location, property-type, price, bedroom, bathroom, and square-footage controls.
- Featured property cards with prices, addresses, listing labels, photo counts, and agent details.
- Service tabs for buying, selling, renting, investing, and commercial real estate.
- Responsive testimonial carousel powered by the bundled Bootstrap JavaScript.
- FAQ accordion covering common buying, selling, and investment questions.
- Contact section with contact cards, a message form, working hours, and social placeholders.
- Responsive navigation, dropdown content, local imagery, Font Awesome icons, Bootstrap styles, and the bundled Exo font.

## Tech stack

- HTML5 for the page structure and content
- CSS3 in `css/style.css` and `css/media.css` for the visual system and responsive rules
- [Bootstrap](https://getbootstrap.com/) styles in `css/bootstrap.min.css` and bundled interactions in `js/bootstrap.bundle.min.js`
- Font Awesome assets bundled in `css/all.min.css` and `webfonts/`
- Exo variable font bundled in `fonts/Exo-VariableFont_wght.ttf`
- Local image and icon assets under `images/`

There is no package manifest, dependency lockfile, build tool, custom JavaScript source, or environment-file template in this snapshot. No package manager installation is required to preview the page.

## Run locally

Because this is a static site, serve the repository root with any local HTTP server. For example, with Python 3:

```bash
git clone --depth 1 https://github.com/zeyadhatem00/Elite-homes.git
cd Elite-homes
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000) in a browser. The entry point is [`index.html`](index.html).

Opening `index.html` directly may work in many browsers, but an HTTP server more closely matches normal static hosting and avoids file-origin differences.

## Project structure

```text
.
├── index.html                    # Complete one-page EliteHomes experience
├── css/
│   ├── all.min.css               # Bundled Font Awesome styles
│   ├── bootstrap.min.css         # Bundled Bootstrap CSS
│   ├── media.css                 # Responsive breakpoint overrides
│   └── style.css                 # Site layout, colors, typography, and components
├── fonts/
│   └── Exo-VariableFont_wght.ttf # Local site font
├── images/                       # Property, background, avatar, and section imagery
├── js/
│   └── bootstrap.bundle.min.js   # Bootstrap components used by the page
├── webfonts/                     # Bundled Font Awesome font files
└── .github/workflows/
    └── static.yml                # GitHub Pages deployment workflow
```

## Behavior and limitations

Bootstrap provides the visible dropdown, mobile navigation, service tabs, testimonial carousel, and FAQ accordion. The search controls and contact form do not submit data in this repository: the form has no configured action or method, and the social icons use placeholder `#` links. Featured-property, service, and contact call-to-action buttons are presentational controls until application logic or a backend is connected.

The property names, prices, counts, testimonials, contact details, and performance figures shown on the page are static content in `index.html`; they are not loaded from a live real-estate service. The repository contains no environment variables or external API configuration to provide.

## Deployment configuration

[`.github/workflows/static.yml`](.github/workflows/static.yml) defines a GitHub Pages workflow that runs on pushes to `main` and on manual dispatch. It uploads the repository root as the Pages artifact. A live deployment URL is not declared in the repository metadata, so this README does not claim one.
