# Open Issues & Recommendations — Site Audit (Feb 2026)

This document lists all remaining issues, broken links, content concerns, and improvement recommendations discovered during the codebase review. Items are categorized by severity.

---

## 🔴 Critical Issues

### 1. Unfilled Placeholders in COVID-DeepNet Blog Posts

**Files Affected:**
- `_posts/2020-10-01-COVIDDEEPNET.md`
- `_projects/2020-10-01-COVIDDEEPNET.md`

These files contain visible "TODO" placeholders that appear on the live site:

| Location | Placeholder Text |
|----------|-----------------|
| "About the paper" section | `(<--I know we thought of publishing from the beginning but to add some spice i wrote that-->)` |
| "Why Technical Domains" section | `morality rate of --%(<--if anybody know that then pl fill this up-->)` |
| Data augmentation section | `please fill up farhan->` |
| Model Architecture section | `for farhan,plz fill up this gap with the diff aug techniques u used->` |
| Dataset section | `[here]` — broken markdown link with no URL |

**Recommendation:** These should either be filled in with actual data or the parenthetical comments should be removed. The `_research/2021-07-06-COVIDDEEPNET.md` version has some of these fixed already — sync the improvements to `_posts/` and `_projects/` versions.

### 2. Wind Analysis Paper — Wrong Google Doc Embed

**File:** `_research/2021-07-06-Wind_Analysis.md`

The iframe embed still points to the COVID analytics Google Doc (`srcid=1jiWwXSEQhL5Jp6ZxyZdoxj2bDSStazwH`), NOT the Wind Energy paper. The correct Google Doc ID for the Wind Analysis paper needs to be inserted.

### 3. COVID-DeepNet Project — Wrong PDF Download Link

**File:** `_projects/2020-10-01-COVIDDEEPNET.md` (line ~180)

The "Complete Article" download link points to `Covid_Decontamination.pdf` instead of the COVID-DeepNet paper. The iframe also embeds the wrong document.

---

## 🟡 Moderate Issues

### 4. Multiple `<body>` Tags in `index.html`

**File:** `index.html`

The homepage uses three separate `<body>` tags (lines ~16, ~47, ~68). Valid HTML should have only one `<body>` element. Replace extra `<body>`/`</body>` pairs with `<div>` or `<section>` elements.

### 5. Default Theme Pages Still Present

The following pages contain unmodified Minimal Mistakes theme content and should either be removed, redirected, or customized:

| File | Issue |
|------|-------|
| `_pages/about.md` | Contains default "Minimal Mistakes" theme description |
| `_pages/sample-page.md` | Contains default "XYZ Doohickey Company" placeholder |
| `_pages/splash-page.md` | Contains "Bacon ipsum" placeholder text |
| `_pages/terms.md` | Contains generic privacy/disclosure policy mentioning affiliate programs and Google Adsense |

### 6. Broken Virtual CV Link

**File:** `_config.yml` (line ~118)

The author sidebar contains a "Virtual CV" link to `/vcv/`, but no such page exists in `_pages/`. This link will result in a 404.

### 7. Filename Misspelling — `_pages/acheivements.md`

**File:** `_pages/acheivements.md`

The filename is misspelled (`acheivements` instead of `achievements`). While the permalink `/achievements/` works correctly, the filename inconsistency could cause confusion for future developers.

### 8. Duplicate `toc: true` in `aboutme.md`

**File:** `_pages/aboutme.md` (lines 3 and 19)

The `toc: true` front matter key is specified twice. Remove the duplicate.

### 9. Recursion Publication — Korean Content

**File:** `_publications/2018-03-01-recursion.md`

This publication page contains Korean language content about recursion algorithms. Unless this is intentional, it appears to be a placeholder/sample from the theme that should be replaced with an actual publication.

### 10. Gallery2 Page — Placeholder Content

**File:** `_pages/gallery2.md`

Contains references to `unsplash-gallery-image-*.jpg` which are default theme images that likely don't exist in the assets folder. The `url:` fields don't match the `image_path:` fields.

---

## 🟢 Minor Issues & Recommendations

### 11. ResearchGate URL Inconsistency

- `_config.yml` uses: `https://www.researchgate.net/profile/Farhan_Hai_Khan` (underscore)
- `docs/ai_generated/general.md` uses: `https://www.researchgate.net/profile/Farhan-Hai-Khan` (hyphen)

Verify which URL resolves correctly (ResearchGate may redirect both, but consistency is preferred).

### 12. "OrcID" Label Misspelling

**File:** `_config.yml` (lines ~132, ~181)

The label says `"OrcID"` but the correct spelling is `"ORCID"` (Open Researcher and Contributor ID).

### 13. Search Not Enabled

**File:** `_config.yml` (line ~63)

`search` is not set to `true`. Enabling search would significantly improve user experience:
```yaml
search: true
search_full_content: true
```

### 14. No Google Analytics Configured

**File:** `_config.yml` (line ~100)

Analytics provider is set to `false`. Consider setting up Google Analytics (or a privacy-respecting alternative like Plausible/Umami) to track site visitors.

### 15. Blog Posts Have Numerous Spelling Errors

The COVID-DeepNet blog posts (both `_posts` and `_research` versions) contain extensive spelling errors throughout. Major recurring ones include:

| Error | Correction |
|-------|-----------|
| `insightfull` | `insightful` |
| `fulfledged` | `full-fledged` |
| `acchives` | `achieves` |
| `Relavent` / `relevent` | `Relevant` |
| `Sience` | `Since` |
| `spreead` / `speading` | `spread` / `spreading` |
| `cuntries` | `countries` |
| `dificult` | `difficult` |
| `invasticate` | `investigate` |
| `indentify` | `identify` |
| `indivisual` | `individual` |
| `treatement` | `treatment` |
| `obsereved` | `observed` |
| `experianced` | `experienced` |
| `robost` | `robust` |
| `accurecy` | `accuracy` |
| `destorted` | `distorted` |
| `intorduced` | `introduced` |
| `seviour` | `severe` |
| `rebust` | `robust` |
| `litrally` | `literally` |
| `munites` | `minutes` |
| `desies` / `deisies` | `disease` / `diseases` |
| `lunges` | `lungs` |
| `robest` | `robust` |
| `failier` | `failure` |
| `baising` / `baised` | `biasing` / `biased` |
| `semntic` | `semantic` |
| `segmentatin` | `segmentation` |
| `whould` | `would` |
| `seperated` | `separated` |
| `channle` | `channel` |
| `divices` | `devices` |
| `michro processer` | `microprocessor` |
| `tranfer` | `transfer` |
| `familier` | `familiar` |
| `valueable` | `valuable` |
| `achived` | `achieved` |

**Note:** These were NOT auto-corrected because many appear in authored blog content that may have been intentionally kept in an informal style. The `_research/` versions have had some corrections applied already. Consider reviewing and updating systematically.

### 16. Deprecated `whitelist` Key in `_config.yml`

**File:** `_config.yml` (line ~278)

Jekyll deprecated `whitelist` in favor of `allowlist`. While this may still work with older versions, consider updating for forward compatibility:
```yaml
allowlist:
  - jekyll-paginate
  - jekyll-sitemap
  ...
```

### 17. Missing Teaser Images for Some Collections

Several research/project entries don't have a `teaser` image set in their front matter, which means they'll show the default fallback teaser (`TeamFKlogo.png`) in grid views. Consider adding specific teasers for:
- `_posts/2020-09-29-covid_decontamination.md`
- `_achievements/2020-11-20-dsciemtechteam.md` (path contains spaces which can cause issues)

### 18. Image Paths with Spaces

Several image paths contain spaces (e.g., `DSC Institute of Engineering & Management Dark Vertical-Logo.png`). While this works, URLs with spaces can cause issues in some browsers or tools. Consider renaming these files to use hyphens or underscores.

### 19. `_pages/Gallery_Wordcloud.txt` — Orphaned File

This text file in the `_pages` directory doesn't appear to be used by any page and may be leftover from development.

### 20. 404 Page Uses Deprecated Google Script

**File:** `_pages/404.md`

The Google `fixurl.js` script (`https://linkhelp.clients.google.com/tbproxy/lh/wm/fixurl.js`) has been discontinued by Google and will not function.

---

## 📊 Content Improvement Suggestions

### A. Homepage Biography — Temporal Language

The biography on `index.html` uses present-tense statements like "currently a part of", "currently guiding students under Winter of Code", "currently working as a Machine Learning Intern at IIT Kharagpur". If these roles have since concluded, the language should be updated to past tense.

### B. Resume Embed — Google Drive Viewer

The resume on `aboutme.md` uses Google Drive's embedded viewer (`docs.google.com/viewer?srcid=...`). This sometimes fails to load. Consider:
1. Hosting the PDF directly in the repo under `assets/`
2. Using a more reliable embed method
3. Adding a direct download link as fallback

### C. Formspree Contact Form

The contact form on `aboutme.md` uses Formspree (`formspree.io/xbjznznp`). Verify that this form ID is still active and receiving submissions.

### D. Consider Removing WoC Prominence from Homepage

The "Winter of Code" section on the homepage is prominent but references a 2020 program. Consider moving it to a less prominent position or archiving it if the program has concluded.

---

## ✅ Architecture Notes

| Aspect | Status |
|--------|--------|
| Remote theme version | `mmistakes/minimal-mistakes@4.24.0` (latest is 4.26.x — consider upgrading) |
| Ruby/Jekyll setup | `Gemfile` looks correct for GitHub Pages |
| Collections | Properly configured: research, projects, courses, achievements, gallery, woc |
| Navigation | Clean, functional navigation in `_data/navigation.yml` |
| Skins | Using "neon" skin — works well for a tech portfolio |
| Plugins | Standard GitHub Pages compatible set |

---

*Generated during automated code review — February 2026*

