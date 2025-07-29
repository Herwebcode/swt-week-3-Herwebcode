# Static Review Summary – Week 3 Assignment

**Reviewer:** Bashirat  
**Date:** July 2025  
**Review Mode:** Static Testing Only (No Code Execution)

---

## ✅ Objective

The purpose of this static code review was to evaluate the `gallery.html` and `requirements.md` files for the image gallery project. Following static testing principles, no files were executed or rendered in a browser. All findings are based on code inspection, HTML/CSS/JS structure, and traceability to requirements.

---

## 🔍 Summary of Key Issues Identified

### 1. Functional Gaps
- No indication that the gallery fully meets **FR2.1** and **FR3.1**, which require image filtering and lightbox interactivity.
- Although JavaScript logic is embedded in the HTML, the structure raises scope-related concerns (e.g., event listeners inside loops without proper closure handling).

### 2. Usability & Accessibility Concerns
- One or more `<img>` tags are missing `alt` attributes, violating **NFR3.3.2** (accessibility requirement).
- Use of `cursor: alias` for clickable elements does not align with standard user expectations; `cursor: pointer` would better indicate interactivity.

### 3. Traceability & Specification Mismatches
- Some requirements, such as accessibility and expected UI feedback, are not clearly addressed in the current codebase.

---

## 🗂 Issues Created (on GitHub)

| Issue Type | Title |
|------------|-------|
| ❌ Failed Test Report | Missing Alt Text for Images (REQ-NFR3.3.2) |
| ❌ Failed Test Report | Incorrect Cursor Usage in CSS (REQ-NFR3.2) |
| ❌ Failed Test Report | Potential Logic Error in Lightbox Click Handler (REQ-FR3.1) |
| 📋 Test Summary Table | Static Review Results Summary |

---

## 💬 Inline Code Review Comments (Pull Request)

1. **HTML Image Tags** – Flagged missing `alt` attribute.
2. **CSS Cursor Rule** – Noted poor UX choice (`cursor: alias`).
3. **JavaScript Lightbox Handler** – Warned about potential closure issue in click event handler inside loop.

---

## 🧠 Reflection

This exercise strengthened my ability to identify issues without relying on execution. It also emphasized the importance of writing code that is readable, traceable to requirements, and logically sound even when not actively running. I now appreciate how static analysis supports early-stage testing and documentation compliance.

  
