# Quick Wins — Easy Improvements You Can Make Today

Low-effort, high-impact changes to improve your site. Sorted by estimated time to complete.

---

## ⚡ 5-Minute Fixes

### 1. Enable Site Search
In `_config.yml`, change:
```yaml
search: true
search_full_content: true
```
This instantly adds a search icon in the masthead that lets visitors search all content.

### 2. Remove Default Theme Pages
Delete (or exclude) these files that show default Minimal Mistakes content:
- `_pages/about.md` (visitors might find this instead of your actual about page)
- `_pages/sample-page.md`
- `_pages/splash-page.md`

### 3. Remove the Broken Virtual CV Link
In `_config.yml`, either:
- Remove the "Virtual CV" entry from author links (line ~117-118), OR
- Create a `/vcv/` page that redirects to an actual CV/resume

### 4. Fix the 404 Page
Remove the broken Google `fixurl.js` script from `_pages/404.md` (the script no longer works). The page text itself is fine.

---

## ⏱️ 15-Minute Improvements

### 5. Clean Up the COVID-DeepNet Post
Open `_posts/2020-10-01-COVIDDEEPNET.md` and:
- Remove inline comments like `(<--I know we thought...-->)`
- Replace `morality rate of --%(<--if anybody...-->)` with the actual mortality rate
- Fill in the augmentation techniques or copy from the `_research/` version
- Fix or remove `[here]` broken link in the Dataset section

### 6. Update Biography Tense
Check if these statements in `index.html` are still current:
- "currently a part of the Artificial Intelligence Technical Team"
- "currently guiding students under Winter of Code"
- "currently working as a Machine Learning Intern at IIT Kharagpur"

Update to past tense for completed roles.

### 7. Fix the Recursion Publication
Replace `_publications/2018-03-01-recursion.md` (Korean content) with an actual publication, or delete the file and the publications collection if not needed.

---

## 🕐 30-Minute Enhancements

### 8. Add OG Images to All Pages
Several pages are missing `og_image` metadata, which means social media previews will use the generic fallback. Add appropriate `og_image:` to front matter of:
- All project pages
- All course pages
- Homepage

### 9. Upgrade the Theme
Update from `mmistakes/minimal-mistakes@4.24.0` to the latest version (4.26.x) for bug fixes and new features. Just change the version in `_config.yml`:
```yaml
remote_theme: "mmistakes/minimal-mistakes@4.26.2"
```

### 10. Customize the Terms/Privacy Page
If you want to keep `_pages/terms.md`, replace the generic affiliate/Adsense language with content relevant to your portfolio site.

---

## 🎯 Impact Matrix

| Fix | Effort | Impact | Priority |
|-----|--------|--------|----------|
| Enable search | 🟢 Trivial | 🔴 High | ⭐⭐⭐⭐⭐ |
| Remove default pages | 🟢 Trivial | 🟡 Medium | ⭐⭐⭐⭐ |
| Fix COVID-DeepNet post | 🟡 Medium | 🔴 High | ⭐⭐⭐⭐⭐ |
| Update biography tense | 🟢 Easy | 🟡 Medium | ⭐⭐⭐⭐ |
| Theme upgrade | 🟡 Medium | 🟡 Medium | ⭐⭐⭐ |
| Add OG images | 🟡 Medium | 🟡 Medium | ⭐⭐⭐ |
| Fix Wind Analysis | 🟢 Easy | 🔴 High | ⭐⭐⭐⭐⭐ |

---

*Generated during automated code review — February 2026*

