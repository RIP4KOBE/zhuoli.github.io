# CLAUDE.md

## Project Overview

Personal academic portfolio website for **Zhuo Li (李卓)**, a third-year Ph.D. student at the CLOVER Lab, The Chinese University of Hong Kong (CUHK), specializing in humanoid robotics. Deployed via GitHub Pages.

---

## Tech Stack

- **Type:** Static HTML/CSS/JS — single `index.html` file, no build step
- **Base Template:** iPortfolio by BootstrapMade (v3.10.0)
- **CSS:** Bootstrap 5.2.3 + `assets/css/style.css`
- **JS:** Vanilla ES6+ (`assets/js/main.js`) + vendored libraries in `assets/vendor/`
- **Deployment:** Push to `master` → live on GitHub Pages

**Do not modify** files under `assets/vendor/` — these are upstream libraries.

---

## File Map

```
index.html              # Entire website — edit this for all content changes
assets/css/style.css    # Custom styles
assets/js/main.js       # Custom JS
assets/img/             # Images and GIFs (robot demos, profile photo)
assets/files/           # PDF CV files (CV_Zhuo_Li_CUHK_Public.pdf)
assets/vendor/          # Third-party libraries — do not edit
forms/                  # PHP contact form stub (requires pro license)
```

---

## Content Editing Guide

All content lives in `index.html`. Sections are identified by `id` attributes.

### Section Map

| Section | HTML id | Description |
|---|---|---|
| Header/Profile | `#header` | Name, photo, social links, nav |
| Hero | `#hero` | Name + tagline |
| About | `#about` | Bio paragraph, contact links |
| Research Interests | `#researchhighlights` | Research focus paragraph |
| Publications | `#publications` | All papers grouped by type |
| Academic Services | `#services` | Journal/conference reviewer lists |
| CV link | nav | Links to `assets/files/CV_Zhuo_Li_CUHK_Public.pdf` |

### Social Links (appear in header and about section)
- Google Scholar: `https://scholar.google.com/citations?user=Vkan_K4AAAAJ&hl=en`
- Twitter/X: `https://x.com/ZhuoLi771402`
- YouTube: `https://www.youtube.com/@kkxx1210`
- Email: `zli@mae.cuhk.edu.hk`

---

## Current Content

### Bio (in `#about`)
Third-year Ph.D. at CLOVER Lab, CUHK. Master's from HUST. Collaborated with Prof. Sylvain Calinon and Prof. Darwin G. Caldwell. Previously interned at UBTECH Robotics. Goal: general-purpose humanoid assistants.

### Research Focus (in `#researchhighlights`)
Embodied intelligence and manipulation skill learning for humanoid robots. Intersection of imitation learning, reinforcement learning, foundation models, and robotics. Emphasis on dexterous grasping, bimanual coordination, and whole-body motion generation.

### Publications

**Peer-Reviewed Journals:**
1. "Language-Guided Dexterous Functional Grasping..." — TASE 2025 — Zhuo Li et al.
2. "Human–Humanoid Robots' Cross-Embodiment Behavior-Skill Transfer..." — RAM 2025 — Junjia Liu, Zhuo Li et al.
3. "Planning Multi-fingered Grasps with Reachability Awareness..." — JIRS 2023 — Zhuo Li et al.
4. "Human-like redundancy resolution..." — Advanced Engineering Informatics 2022 — Shiqi Li, ..., Zhuo Li et al.

**Journals in Review:**
1. "Towards Deploying VLA without Fine-Tuning: Plug-and-Play Inference-Time VLA Policy Steering via Embodied Evolutionary Diffusion" — Submitted to RAL 2025 — Zhuo Li et al.

**Conference Papers:**
1. "ManiDP: Manipulability-Aware Diffusion Policy..." — IROS 2025 — Zhuo Li et al.
2. "Instruction-following Long-horizon Manipulation by LLM-Empowered Symbolic Planner" — ROBIO 2024 — Zhihao Li, ..., Zhuo Li et al.

### Academic Services (in `#services`)
**Journal Reviewer:** TASE, RA-L, RAM, TCDS
**Conference Reviewer:** ICRA, IROS, Humanoids, CASE

---

## Publication HTML Pattern

When adding a new publication, follow this structure (adapt from existing entries):

```html
<!-- Paper entry -->
<div class="row publication-item">
  <div class="col-lg-3">
    <img src="assets/img/YOUR_FIGURE.png" class="img-fluid" alt="">
    <!-- or a GIF/video thumbnail -->
  </div>
  <div class="col-lg-9">
    <h5>PAPER TITLE 🆒</h5>
    <p><em>Author1, Author2, ...</em></p>
    <p><strong>Venue Name (ABBR), YEAR</strong></p>
    <p>Abstract text here.</p>
    <p>
      <a href="PAPER_URL">[Paper]</a> /
      <a href="VIDEO_URL">[Video]</a> /
      <a href="PROJECT_URL">[Project Website]</a>
    </p>
  </div>
</div>
```

Emoji legend used in publications:
- 🆒 — Highlights
- `*` — Equal Contribution
- `†` — Project Lead
- `⚡` — Equal Advising

---

## Common Tasks

**Add a new publication:**
1. Add a paper figure/GIF to `assets/img/`
2. Insert a new entry in `#publications` under the appropriate subsection (Journals / In Review / Conference)

**Update CV:**
1. Replace `assets/files/CV_Zhuo_Li_CUHK_Public.pdf` with the new file (keep the same filename, or update all references)

**Update bio or research description:**
- Edit the paragraph text in `#about` or `#researchhighlights`

**Add a new section (Honors, Talks):**
- These sections exist in the nav but are currently hidden/commented out in the HTML — uncomment and populate as needed