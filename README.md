# Architecture Tour Tracker (Unirate)

A lightweight, mobile-first web app designed for evaluating and comparing university architecture schools during open days. Built to run cleanly in any mobile browser or as a standalone Progressive Web App (PWA) on an iPhone home screen, completely offline.

**Live Web App:** [https://declanclem.github.io/Unirate/](https://declanclem.github.io/Unirate/)

---

## Purpose & Focus

Architecture degrees carry practical demands that generic university guides often overlook. This tracker focuses on core spatial and studio realities:

* **Desk Allocations:** Permanent assigned desks vs. hot-desking.
* **Studio Culture & Crits:** Constructive feedback vs. adversarial review culture.
* **Technical Balance:** Demands on structural maths/engineering for students entering from an Art background.
* **Hidden Costs:** Plotting, 3D printing filaments, casting, and workshop materials.
* **ARB Accreditation:** Clarifying qualification status amid ongoing ARB structural updates.
* **Work-Life & Athletics:** All-nighter culture vs. protected time for sports clubs (e.g. Wednesday afternoons).

---

## Low-Cognitive-Load Prompt Set

All questions are intentionally capped at **10 words or fewer** to allow low-friction, rapid asking and quick-tap recording during busy tours:

### Academic Staff & Admissions Tutors
1. *"Is this school mostly artistic, technical, or research focused?"* (9 words)
2. *"With the new ARB structure, what qualification do we get?"* (10 words)
3. *"How are crits run, and is feedback constructive?"* (8 words)
4. *"How much engineering maths is needed with an Art background?"* (10 words)

### Current Students (Reality Checks)
5. *"Do you get your own permanent desk all year?"* (9 words)
6. *"How much do you spend on materials and printing?"* (9 words)
7. *"Are queues for workshop equipment bad before deadlines?"* (8 words)
8. *"Do students here regularly have to pull all-nighters?"* (9 words)
9. *"Are Wednesday afternoons actually kept free for sports?"* (8 words)

---

## iPhone Setup (Add to Home Screen)

To use as a standalone app with no App Store installation:

1. Open `https://declanclem.github.io/Unirate/` in **Safari** on iPhone.
2. Tap the **Share** button (the square icon with the upward arrow at the bottom).
3. Scroll down and select **Add to Home Screen**.
4. Tap **Add**.

The app will now launch directly from the home screen, run full-screen without browser chrome, and save all data locally on the device (`localStorage`) even without cellular coverage.

---

## Technical Architecture

* **Zero Dependencies:** Single self-contained HTML5, CSS3, and modern JavaScript file (`index.html`).
* **Persistence:** Client-side HTML5 `localStorage` (no backend database or sign-in required).
* **Views:**
  * **Saved Unis:** Card directory showing dates, desk allocation, and ratings, with edit/delete capability.
  * **+ Add Uni:** Form optimized for mobile touch targets with chip selectors and numeric rating dials.
  * **Compare:** Multi-column responsive matrix displaying side-by-side criteria for all logged universities.
