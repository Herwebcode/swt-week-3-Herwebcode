# 📝 Static Review Summary

## ✅ What I Reviewed

I reviewed:

- `requirements.md`: The functional and non-functional specs for a basic image gallery
- `gallery.html`: The HTML/CSS layout for the gallery (pull request titled "Feature: Buggy Image Gallery")

## 🐛 Types of Issues Found

- **Documentation issues:** Vagueness in feature definitions (e.g., what "look good visually" entails)
- **Code issues:**
  - Missing JavaScript logic for gallery/filter functionality
  - Incorrect use of cursor styling (`alias` instead of `pointer`)
  - Missing `alt` text on images (accessibility violation)

## 💭 Reflection on Static Testing

### Question 1: Documentation Review

- Most features are defined, but some are vague or overlap (FR1.3, FR3.1/3.3).
- I suggested more precise wording and raised a GitHub Issue titled “Ambiguity in Requirements Phrasing”.
- I commented on the need for clarity in how filters reset and how accessibility is ensured.

### Question 2: Code Review

1. **Missing JavaScript**: I flagged that the gallery has no JS implementation, making filtering/lightbox non-functional.
2. **Cursor Confusion**: I suggested changing `cursor: alias` to `pointer` for expected close-button behavior.
3. **Accessibility**: I noted that images need `alt` text for screen readers, per NFR3.3.2.

### Question 3: Reflection

- The lack of JS made it harder to understand the full gallery logic from static code.
- I noticed some assumptions in the requirements — for example, whether responsiveness is expected.
- The static review helped me better understand how _good specs and semantic code_ improve maintainability and accessibility.

---

Overall, I learned that even without running code, many problems can be identified through careful reading — especially related to clarity, accessibility, and maintainability.
