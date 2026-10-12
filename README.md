<div align="center">

# GDGC Playground

### Your game. Your challenge. Your playground.

An interactive online arcade for discovering games, exploring challenges, and playing supported titles in your browser.

[![React](https://img.shields.io/badge/React-bundled-61DAFB?logo=react&logoColor=20232A)](https://react.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4.1.12-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Vercel](https://img.shields.io/badge/Hosted_on-Vercel-000000?logo=vercel&logoColor=white)](https://vercel.com/)

**[▶ Visit the live playground](https://gdgc-playground.vercel.app/)**

</div>

---

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Screenshots](#screenshots)
- [Technology](#technology)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [How to Use](#how-to-use)
- [Game Controls](#game-controls)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [Proposed Roadmap](#proposed-roadmap)
- [Acknowledgements](#acknowledgements)
- [License](#license)
- [Developer](#developer)

## Project Overview

GDGC Playground brings a collection of browser-accessible games together in one arcade-style website. Visitors can browse the catalog, open supported games, and find the site's About, FAQ, and Contact sections from the interface.

The project is intended for players who want a quick way to explore web games, and for developers interested in an interactive React interface with a game catalog and hosted assets. Its current repository is a **production-site snapshot**: it contains the built application and static files, not the original component source or build setup.

## Features

Features visible in the current site and compiled application include:

- A responsive arcade-themed home page and game catalog.
- Game cards with a play action and game details.
- Catalog titles including Pattern Mind, Redline Rush, Stride Runner, Car Factory Escape, Neon Gravity, LaneMastersArcade, Flipslide Puzzle, Overdrive Shooter, Hidden Object Game, Stickman Sniper, Crimson Hawk, Dots and Boxes Game, and Lumenfall.
- About Us, FAQ, and Contact Support content and navigation.
- Sign-in, account, favorites, and admin-panel interface flows in the compiled app; access to service-dependent actions may require the original backend configuration.
- Footer links to social profiles and site sections.

Game availability and service-dependent actions can change independently of this repository snapshot. Visit the [live site](https://gdgc-playground.vercel.app/) for the current experience.

## Screenshots

No website screenshots are included in this repository. The live preview is the most accurate way to see the current interface: **[open GDGC Playground](https://gdgc-playground.vercel.app/)**.

To add genuine screenshots, capture the live site in a browser at desktop and mobile viewport sizes, then commit the captures in the repository and link them here. No mock screenshots are used in this README.

## Technology

| Area | Verified information |
| --- | --- |
| UI runtime | React and React DOM are included in the compiled JavaScript bundle. |
| Styling | Tailwind CSS 4.1.12 is identified in the generated stylesheet. |
| Icons | Lucide icon components are present in the application bundle. |
| Fonts | The HTML references Fontshare font families; the stylesheet also imports Inter from Google Fonts. |
| Hosting | Vercel; `vercel.json` rewrites the root and `/assets/*` requests to the static site directory. |
| External assets | Game artwork is present under the repository's Supabase Storage path; the compiled app also references Supabase endpoints. |

The original package manifest, exact dependency versions, framework build configuration, and source modules are not present, so the build tool and complete dependency list cannot be verified from this checkout.

## Project Structure

This tree describes the files present in the repository. Generated font and game-image filenames are abbreviated for readability.

```text
.
├── CDN/wf/                         # Cached font files
├── _DataURI/                       # Image data captured as text files
├── api.fontshare.com/v2/css.css    # Cached Fontshare stylesheet
├── gdgc-playground/
│   ├── index.html                  # Static application entry document
│   └── assets/
│       ├── index-9f1ce1a8.js       # Compiled React application bundle
│       ├── index-us4KDYrd.css      # Generated application stylesheet
│       └── ...                     # Game and brand artwork
├── google api fonts/css2.css       # Cached Google Fonts stylesheet
├── playground/search/warmup.html   # Captured search warmup page
├── supabase/storage/v1/object/
│   └── public/game-files/          # Game thumbnail assets
├── .gitignore
└── vercel.json                     # Vercel route rewrites
```

The repository does not contain `src/`, `package.json`, a lockfile, `vite.config.*`, or a `LICENSE` file. Empty `src/` and `public/` folders may exist in a local workspace as untracked placeholders; Git does not preserve empty directories. They are not part of the tracked application source.

## Getting Started

### Prerequisites

- Git.
- Node.js and npm only if you plan to use the Vercel CLI for local preview or deployment.

### Clone the repository

```bash
git clone https://github.com/vinu4545/GDGC_playground.git
cd GDGC_playground
```

### Local preview

This checkout has no `package.json` or application source, so there is no verified `npm install`, `npm run dev`, or `npm run build` command. The repository is configured for Vercel static routing. To preview it through those rewrites, authenticate and link the project with the Vercel CLI, then run:

```bash
npx vercel login
npx vercel link
npx vercel dev
```

The Vercel project link in `.vercel/` is local-only and ignored by Git, so a fresh clone may need to be linked again. Application environment-variable names cannot be established from the compiled snapshot. Do not copy or publish values from local `.env*` files.

## How to Use

1. Open the [live playground](https://gdgc-playground.vercel.app/).
2. Browse the game catalog and select a title.
3. Use that game's play action to launch it.
4. Follow the instructions shown by the selected game; controls and gameplay may differ by title.
5. Use the site navigation or footer to visit About, FAQ, and Contact sections.

## Game Controls

There is no verified, site-wide control mapping in this repository. Controls are game-specific; follow the instructions shown by each game after launch.

## Deployment

The root `vercel.json` maps `/` to `gdgc-playground/index.html` and `/assets/*` to the built assets directory. After installing or invoking the Vercel CLI and linking an account/project, deploy a preview or production build with:

```bash
npx vercel
npx vercel --prod
```

The live deployment is [gdgc-playground.vercel.app](https://gdgc-playground.vercel.app/). No CI workflow is included in this repository snapshot.

## Contributing

Contributions are welcome. Keep changes focused, preserve the existing live-site behavior, and describe what was tested. Since the source application and build configuration are not included, changes to the compiled bundle should be made with care; whenever possible, contribute against the original source project.

```bash
# Fork the repository on GitHub, then clone your fork:
git clone https://github.com/<your-github-username>/GDGC_playground.git
cd GDGC_playground
git switch -c your-feature-name
# Make and verify a focused change
git add <changed-files>
git commit -m "Describe your change"
git push -u origin your-feature-name
```

Then open a pull request with a clear summary and verification notes. Replace `<your-github-username>` with your GitHub username.

## Proposed Roadmap

These are ideas, not committed plans:

- Restore and document the original application source and reproducible build setup.
- Add genuine desktop and mobile screenshots.
- Document game-specific controls and accessibility information.
- Continue improving game discovery and the catalog as the collection grows.

## Acknowledgements

- React for the UI runtime.
- Tailwind CSS for the generated styling system.
- Lucide for the icon components present in the bundle.
- Vercel for hosting and routing.

The original creators and reuse terms for individual games and some artwork are not documented in this snapshot. Verify their attribution and licenses before redistributing those assets.

## License

No `LICENSE` file was found in this repository. Reuse, modification, and redistribution permissions therefore need to be clarified with the project owner; do not assume the project is under an open-source license.

## Developer

**Developed by Vinay**

Built with creativity, curiosity, and a passion for interactive gaming.

- [LinkedIn](https://www.linkedin.com/in/vinay-gaddam45/)
- [GitHub repository](https://github.com/vinu4545/GDGC_playground)

## Ready to Play?

Step into GDGC Playground, explore the games, and help make the arcade better.

**[Play now →](https://gdgc-playground.vercel.app/)**
