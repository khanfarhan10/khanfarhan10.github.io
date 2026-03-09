# Blog Content Review — Quality Assessment

A detailed review of all blog posts, research articles, and project pages with recommendations for improvement.

---

## Content Duplication Matrix

Several pieces of content exist in multiple locations with varying levels of quality. Here's the mapping:

| Content | `_posts/` | `_projects/` | `_research/` | Best Version |
|---------|-----------|--------------|--------------|-------------|
| COVID Decontamination | ✅ `2020-09-29` | — | ✅ `2020-09-29` | `_research/` (has MathJax) |
| COVID-DeepNet | ✅ `2020-10-01` | ✅ `2020-10-01` | ✅ `2020-10-01` | `_research/` (most polished) |
| COVID Analytics | — | — | ✅ `2021-01-29` | Only one copy |
| Wind Analysis | — | — | ✅ `2021-07-06` | ⚠️ Wrong abstract |
| Data Science (Dim. Reduction) | — | — | ✅ `2021-07-08` | Only one copy |

### Recommendation
- **COVID-DeepNet** exists in 3 places. The `_research/` version is the most up-to-date (has Springer citation, fixed some spelling). The `_posts/` and `_projects/` versions still contain raw TODOs and unfilled placeholders. Either:
  - Sync improvements from `_research/` to the other versions, OR
  - Remove the duplicates and keep only the `_research/` version
- **COVID Decontamination** `_posts/` version uses WMF images (`image8.wmf`, etc.) which won't render in browsers. The `_research/` version uses MathJax equations instead — much better.

---

## Blog Post Quality Scores

### ⭐⭐⭐⭐⭐ Excellent — Ready for Public

| Article | File |
|---------|------|
| COVID Decontamination (Research) | `_research/2020-09-29-covid_decontamination.md` |
| Dimensionality Reduction (Research) | `_research/2021-07-08-Data-Science.md` |

These are well-structured, properly formatted, and contain good academic content.

### ⭐⭐⭐⭐ Good — Minor Polish Needed

| Article | File | Notes |
|---------|------|-------|
| COVID-DeepNet (Research) | `_research/2020-10-01-COVIDDEEPNET.md` | Some informal language, minor spelling. Has Springer citation. |
| COVID Analytics (Research) | `_research/2021-01-29-covid_analysis.md` | Minimal content — just abstract + iframe embed. |

### ⭐⭐ Needs Significant Work

| Article | File | Issues |
|---------|------|--------|
| COVID-DeepNet (Post) | `_posts/2020-10-01-COVIDDEEPNET.md` | Unfilled placeholders, internal comments visible |
| COVID-DeepNet (Project) | `_projects/2020-10-01-COVIDDEEPNET.md` | Same as above + wrong PDF link |
| Wind Analysis | `_research/2021-07-06-Wind_Analysis.md` | Wrong abstract, wrong iframe embed |

### ⭐ Skeleton/Placeholder

| Article | File | Issues |
|---------|------|--------|
| COVID Decontamination (Post) | `_posts/2020-09-29-covid_decontamination.md` | WMF images won't display |
| Starter Blog (WoC) | `_woc/2020-12-18-StarterBlog.md` | Template content with "Blah Blah Blah" |

---

## COVID-DeepNet — Detailed Spelling Comparison

The `_research/` version has been partially cleaned up compared to `_posts/` and `_projects/`. Here are improvements that exist in `_research/` but NOT in the other versions:

| Section | `_posts/`/`_projects/` | `_research/` |
|---------|----------------------|-------------|
| Title section | Contains inline comment `(<--I know...)` | Comment removed |
| Mortality rate | `morality rate of --%(<--if anybody...-->)` | Fixed to `mortality rate of 0.28%` |
| Augmentation | `please fill up farhan->` placeholder | Filled in with CLAHE, Horizontal Flipping, etc. |
| Dataset link | `[here]` (broken) | `[here]` still broken (both need fixing) |
| "About the paper" | `insightfull` → not fixed | Fixed to `insightful` |
| General | `fulfledged` | `full-fledged` |
| General | `acchives` | `acchives` (still wrong in both — should be "achieves") |
| Author attribution | Not attributed | `author: Soumyadip Sarkar` added |
| Publication link | Not present | Springer link added |
| "Complete Article" | Wrong PDF (Decontamination) | Correct link to Springer |

---

## Project Pages Assessment

| Project | Teaser | Content Quality | Links Working |
|---------|--------|----------------|---------------|
| COVID-DeepNet | ✅ | ⚠️ Placeholders | ⚠️ Wrong PDF |
| AutoMailer | ✅ | ✅ Minimal but clean | ✅ |
| Car Damage Detection | ✅ | ✅ Detailed | ✅ |
| Colour Splash | ✅ | ✅ Very detailed (notebook export) | ✅ |
| Mass Certificate Generator | ? | ? | ? |
| MRCNN Demo | ? | ? | ? |
| Neural Style Transfer | ? | ? | ? |
| SolarTracker | ? | ? | ? |
| Vaccine Notifier | ? | ? | ? |

---

## Top Priority Actions

1. **Remove or fill placeholders** in `_posts/2020-10-01-COVIDDEEPNET.md` and `_projects/2020-10-01-COVIDDEEPNET.md`
2. **Fix Wind Analysis** abstract and iframe in `_research/2021-07-06-Wind_Analysis.md`
3. **Fix COVID-DeepNet Project** download link (points to wrong PDF)
4. **Remove WMF images** from `_posts/2020-09-29-covid_decontamination.md` (replace with MathJax or PNGs)
5. **Update temporal references** in biography (homepage) if roles have changed

---

*Generated during automated code review — February 2026*

