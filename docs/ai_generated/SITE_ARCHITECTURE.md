# Site Architecture Overview

A quick reference guide to the structure and content organization of `khanfarhan10.github.io`.

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Static Site Generator | Jekyll |
| Theme | [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) v4.24.0 (remote) |
| Skin | `neon` |
| Hosting | GitHub Pages |
| Domain | `https://khanfarhan10.github.io` |

---

## Directory Map

```
khanfarhan10.github.io/
├── _config.yml              # Main site configuration
├── index.html               # Homepage (layout: home)
├── Gemfile                  # Ruby dependencies
│
├── _data/
│   ├── authors.yml          # Author profiles (for multi-author posts)
│   ├── navigation.yml       # Top navigation bar links
│   └── ui-text.yml          # UI text translations
│
├── _pages/                  # Standalone pages
│   ├── aboutme.md           # /aboutme/ — Main about page with resume & contact
│   ├── about.md             # /about/ — ⚠️ Default theme content (unused?)
│   ├── acheivements.md      # /achievements/ — Achievements grid
│   ├── courses.md           # /courses/ — Courses grid
│   ├── gallery.md           # /gallery/ — Photo gallery (splash layout)
│   ├── gallery2.md          # /gallery2/ — ⚠️ Dev/test gallery page
│   ├── posts.md             # /posts/ — Blog feed
│   ├── projects.md          # /projects/ — Projects grid
│   ├── research.md          # /research/ — Research articles grid
│   ├── sitemap.md           # /sitemap/ — HTML sitemap
│   ├── woc.md               # /WoC/ — Winter of Code
│   ├── 404.md               # 404 error page
│   ├── sample-page.md       # ⚠️ Default theme sample
│   ├── splash-page.md       # ⚠️ Default theme sample
│   └── terms.md             # ⚠️ Default theme terms/privacy
│
├── _posts/                  # Blog posts (date-prefixed)
│   ├── 2020-09-29-covid_decontamination.md
│   └── 2020-10-01-COVIDDEEPNET.md
│
├── _research/               # Research collection
│   ├── 2020-09-29-covid_decontamination.md
│   ├── 2020-10-01-COVIDDEEPNET.md
│   ├── 2021-01-29-covid_analysis.md
│   ├── 2021-07-06-Wind_Analysis.md
│   └── 2021-07-08-Data-Science.md
│
├── _projects/               # Projects collection
│   ├── 2020-10-01-COVIDDEEPNET.md
│   ├── 2020-11-25-AutoMailer-Python.md
│   ├── 2020-11-25-Car-Damage-Detection.md
│   ├── 2020-11-25-Colour-Splash-Effect.md
│   ├── 2020-11-25-Mass-Certificate-Generator-Python.md
│   ├── 2020-11-25-MRCNN-Demo.md
│   ├── 2020-11-25-Neural-Style-Transfer.md
│   ├── 2020-11-25-SolarTracker.md
│   └── 2020-11-25-Vaccine-Availability-Notifier.md
│
├── _courses/                # Courses collection
│   ├── 2021-07-05-py4e-specialization.md
│   ├── 2021-07-06-pythonforresearch.md
│   └── 2021-07-07-ibm-specialization.md
│
├── _achievements/           # Achievements collection
│   └── 2020-11-20-dsciemtechteam.md
│
├── _publications/           # Publications collection
│   └── 2018-03-01-recursion.md   # ⚠️ Korean content — likely sample
│
├── _woc/                    # Winter of Code collection
│   ├── 2020-12-18-StarterBlog.md
│   ├── Weekly_blogs.md
│   ├── Welcome to my WoC blog.md
│   └── WoCabulary.md
│
├── _includes/               # HTML partials (theme overrides)
├── _layouts/                # Layout templates (theme overrides)
├── _sass/                   # SCSS stylesheets (theme overrides)
│
├── assets/
│   ├── css/main.scss        # Main stylesheet entry
│   ├── images/              # All site images (~141 files)
│   └── js/                  # JavaScript files
│
├── docs/                    # Theme documentation (excluded from build)
│   └── ai_generated/        # AI-generated documentation
│
└── PDF_docs/                # Downloadable PDFs
    └── Covid_Decontamination.pdf
```

---

## Navigation Structure

```
[Research] → /research/      (collection grid)
[Projects] → /projects/      (collection grid)
[Achievements] → /achievements/  (collection grid)
[Courses] → /courses/        (collection grid)
[Feed] → /posts/             (blog posts by tag)
[Photos] → /gallery/         (splash photo gallery)
[About] → /aboutme/          (bio, resume, contact form)
```

---

## Collections Configuration

| Collection | Output | Items | Permalink Pattern |
|-----------|--------|-------|-------------------|
| `research` | ✅ | 5 | `/:categories/:title/` |
| `projects` | ✅ | 9 | `/:categories/:title/` |
| `courses` | ✅ | 3 | `/:categories/:title/` |
| `achievements` | ✅ | 1 | `/:categories/:title/` |
| `gallery` | ✅ | 0 | `/:categories/:title/` |
| `woc` | ✅ | 4 | `/:categories/:title/` |

---

## Author/Social Links (Sidebar)

| Platform | URL |
|----------|-----|
| Google Scholar | `https://scholar.google.com/citations?hl=en&user=-HE1HT4AAAAJ` |
| Gmail (Research) | `njrfarhandasilva10@gmail.com` |
| Gmail (General) | `khanfarhanpro@gmail.com` |
| LinkedIn | `https://www.linkedin.com/in/fkpro/` |
| GitHub | `https://github.com/khanfarhan10` |
| ORCID | `https://orcid.org/0000-0001-9854-760X` |
| ResearchGate | `https://www.researchgate.net/profile/Farhan_Hai_Khan` |
| Twitter | `https://twitter.com/itsmetheswagger` |
| StackOverflow | `https://stackoverflow.com/users/12464709/farhan-khan` |
| Instagram | `https://www.instagram.com/i.am.the.swagger/` |
| Facebook | `https://www.facebook.com/khanfarhanh/` |
| Discord | `https://discord.gg/2xzxCUY` |

---

## Pages Flagged for Cleanup

These pages contain default Minimal Mistakes content and can likely be removed:

- `_pages/about.md` — Default theme about page
- `_pages/sample-page.md` — WordPress-style placeholder
- `_pages/splash-page.md` — Theme demo with bacon ipsum
- `_pages/terms.md` — Generic privacy policy template
- `_publications/2018-03-01-recursion.md` — Korean language CS content (theme sample)

---

*Generated during automated code review — February 2026*

