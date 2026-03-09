# Fixes Made - Automated Code Review (Feb 2026)

This document logs all the minor fixes that were directly applied to the codebase.

---

## 1. Footer Social Links Swapped (`_config.yml`)

**File:** `_config.yml` (lines ~188-191)

**Problem:** The Facebook footer link pointed to Instagram's URL and vice versa.

**Before:**
```yaml
- label: "Facebook"
  url: "https://instagram.com/i.am.the.swagger"   # WRONG
- label: "Instagram"
  url: "https://facebook.com/khanfarhanh"          # WRONG
```

**After:**
```yaml
- label: "Facebook"
  url: "https://www.facebook.com/khanfarhanh/"
- label: "Instagram"
  url: "https://www.instagram.com/i.am.the.swagger/"
```

---

## 2. Spelling Errors in Homepage (`index.html`)

**File:** `index.html`

| Line | Before | After |
|------|--------|-------|
| ~31 | `acheivements` | `achievements` |
| ~37 | `whereever` | `wherever` |
| ~41 | `varius` | `various` |

---

## 3. Gender Pronoun Error in Homepage (`index.html`)

**File:** `index.html` (line ~89)

**Before:** "has contributed to **her** most recent success"
**After:** "has contributed to **his** most recent success"

---

## 4. Gender Pronoun Errors in About Page (`_pages/aboutme.md`)

**File:** `_pages/aboutme.md` (line ~37)

**Before:**
- "has contributed to **her** most recent success"
- "he vastly improved the productivity of **her** team"

**After:**
- "has contributed to **his** most recent success"
- "he vastly improved the productivity of **his** team"

---

## 5. Spelling Errors in About Page (`_pages/aboutme.md`)

**File:** `_pages/aboutme.md` (line ~35)

| Before | After |
|--------|-------|
| `pursueing` | `pursuing` |
| `wth` | `with` |

---

## 6. Broken Link — `www.khanfarhan10.github.io` (`index.html`)

**File:** `index.html` (line ~96)

**Before:** `https://www.khanfarhan10.github.io` (GitHub Pages doesn't support `www.` subdomain by default)
**After:** `https://khanfarhan10.github.io`

---

## 7. HTTP to HTTPS — GitHub Link (`index.html`)

**File:** `index.html` (line ~55)

**Before:** `http://github.com/khanfarhan10/TextSentimentAnalysis`
**After:** `https://github.com/khanfarhan10/TextSentimentAnalysis`

---

## 8. Invalid HTML `</br>` Tags (`index.html`)

**File:** `index.html` (lines ~26, ~50, ~62)

**Before:** `</br>` (not valid HTML)
**After:** `<br>` (correct self-closing tag)

---

## 9. Typo in Research Page (`_pages/research.md`)

**File:** `_pages/research.md` (line ~8)

**Before:** `Emminent Journals`
**After:** `Eminent Journals`

---

## 10. Typo in Courses Page (`_courses/2021-07-05-py4e-specialization.md`)

**File:** `_courses/2021-07-05-py4e-specialization.md` (line ~35)

**Before:** `Data Strcutures and Algorithms`
**After:** `Data Structures and Algorithms`

---

## 11. Wrong Tags on Colour Splash Project (`_projects/2020-11-25-Colour-Splash-Effect.md`)

**File:** `_projects/2020-11-25-Colour-Splash-Effect.md`

**Before:** Tags listed Solar Tracker, BioMimicry, Arduino, etc. (copy-pasted from SolarTracker project)
**After:** Tags now correctly reflect: Computer Vision, Deep Learning, Instance Segmentation, Mask R-CNN, Image Processing, Python

---

## 12. Wrong Abstract in Wind Analysis Research (`_research/2021-07-06-Wind_Analysis.md`)

**File:** `_research/2021-07-06-Wind_Analysis.md`

**Problem:** The abstract was copy-pasted from the COVID-19 Analytics paper instead of the actual Wind Energy paper.
**Fix:** Replaced with a placeholder abstract matching the Wind Energy topic. *Note: The actual abstract from the IEEE publication should be inserted here.*

---

## 13. Missing `mailto:` in Authors Data (`_data/authors.yml`)

**File:** `_data/authors.yml` (line ~24)

**Before:** `url: "dineshrajput828282@gmail.com"`
**After:** `url: "mailto:dineshrajput828282@gmail.com"`

---

## Summary

| Category | Count |
|----------|-------|
| Swapped URLs | 1 |
| Spelling/Typo Fixes | 6 |
| Pronoun Errors | 2 (across 2 files) |
| Broken/Invalid Links | 2 |
| Invalid HTML | 1 (3 instances) |
| Wrong Metadata/Tags | 2 |
| Missing Protocol | 1 |
| **Total Fixes** | **15** |

