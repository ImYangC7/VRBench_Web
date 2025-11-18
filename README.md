# VR-Bench Project Page 🧩

This repository contains the source code of the **VR-Bench** project page:

> **VR-Bench: The First Evaluation of Video Models' Reasoning Abilities through Maze-Solving Tasks**

The page is built on top of Vue 3 and the original academic-project-page template, and customized for VR-Bench with interactive visualizations, benchmark results and dataset links.

---

## 🔗 Related Resources

- **Paper**: VR-Bench – Video Models’ Reasoning Abilities via Maze-Solving (title of the project page)
- **Code**: https://github.com/ImYangC7/VR-Bench  
- **Dataset (Hugging Face)**: https://huggingface.co/datasets/amagipeng/VR-Bench

The top banner of this site also exposes quick-entry buttons for Code and Dataset.

---

## 🧱 Features on This Page

This project page currently includes (but is not limited to) the following sections:

- **Title & Authors**
  - Gradient-styled *VR-Bench* title.
  - Full author list with affiliation superscripts.
  - Affiliation list with one slot per logo (logos can be added later).
  - Equal-contribution and corresponding-author note, plus MetaGPT logo.

- **Overview**
  - An *Overview* section displaying the high-level explainer figure of VR-Bench.

- **Abstract**
  - Abstract rendered from `src/components/mds/abstract.mdx`, supporting Markdown and inline formulas.

- **Maze Carousel**
  - Two-row auto-scrolling gallery of maze instances.
  - First row uses `public/front/1.png`–`10.png`, scrolling left.
  - Second row uses `public/front/11.png`–`20.png`, scrolling right.

- **Bench (Radar Charts)**
  - Four interactive radar charts for **EM**, **SR**, **PR**, **SD** across five tasks (*Base*, *Irreg*, *Trap*, *3D*, *Soko*).
  - A button group allows selecting which metric to view.
  - The enlarged chart at the bottom includes a two-row legend and tooltips that show raw values for each model and task.

- **Maze Variations**
  - A dedicated section titled **Maze Variations**, showing `public/domain_vary.jpg` with a card-style frame.

- **3D & Gaussian Splatting**
  - Sections for 3D models and Gaussian Splatting visualizations (placeholders can be customized with your own assets).

- **BibTeX**
  - A BibTeX block that can be clicked to copy the citation to clipboard.

Comment system and some template demo components have been removed to keep the page concise and focused on VR-Bench.

---

## 🛠 Tech Stack

- **Frontend Framework**: Vue 3
- **Build Tool**: Vite
- **UI Library**: Element Plus
- **Charts**: ECharts (via `vue-echarts`)
- **Markdown & Math**:
  - MDX (`@mdx-js/rollup`) + `remark-math` + `rehype-katex`
- **3D / 3DGS**:
  - `@mkkellogg/gaussian-splats-3d`
  - `vue-3d-loader`

---

## ▶️ Local Development

Prerequisites:

- Node.js ≥ 16
- npm (or pnpm / yarn)

Install dependencies:

```bash
npm install
```

Start a dev server:

```bash
npm run dev
```

This will start the Vite dev server (by default on `http://localhost:5173/`). You can then edit the components and MDX files and see changes live.

Build for production:

```bash
npm run build
```

Preview the built site locally:

```bash
npm run preview
```

---

## 🔧 How to Customize VR-Bench Page

- **Title & Buttons**: `src/components/sections/Title.vue`
  - Change main title, subtitle, authors, affiliations.
  - Update Code / Dataset links and button texts.

- **Abstract**: `src/components/mds/abstract.mdx`
  - Edit the abstract using Markdown (and KaTeX-style math where needed).

- **Carousel Images**: `public/front/*.png` & `src/components/sections/Carousel.vue`
  - Replace images in `public/front` or adjust which files are referenced in `row1Images` / `row2Images`.

- **Bench Radar Charts**: `src/components/sections/Bench.vue`
  - The metric values for each model and task are encoded in the `MODELS_DATA` object.
  - To add/remove models or adjust metric values, edit this object and the color mapping if needed.

- **Maze Variations Figure**: `public/domain_vary.jpg` & `src/components/sections/MazeVariations.vue`
  - Replace the image file or adjust the styling of the card.

- **BibTeX**: `src/components/sections/BibTeX.vue`
  - Update the BibTeX array to match the final VR-Bench paper citation.

---

## 📄 License

This repository is based on the original `academic-project-page-template-vue` by Junyao Hu, and has been customized for the VR-Bench project.  
Please refer to the original template repository for website license details if needed.

If you build on top of this page, please keep an appropriate attribution to both the **VR-Bench** project and the original template author.
*** End Patch```github_uploaded ***!
"# VRBench_Web" 
