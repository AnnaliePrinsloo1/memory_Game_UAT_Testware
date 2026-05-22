# User Acceptance Test (UAT) Plan: Memory Game (Beta)

**Project Name:** Memory Game App Validation  
**Test Level:** User Acceptance Testing (UAT) / Beta Phase  
**Version:** Aligned with ISTQB® Foundation Level Syllabus v4.0.1  
**Author:** Annalie Prinsloo 

---

## 1. Introduction & Test Objectives
The Memory Game is a ADHD-friendly, Google teacher approved educational game designed to build visual, verbal and associative memory. The primary objective of testing is to ensure a stable, calm and zero-stalls user experience. Because the application targets children, teenages and adults with ADHD, software bugs like erratic audio, sudden animation flashes or broken progression screens represent high risks fot sensory overstimulations and loss of user focus.

---

## 2. Test Scope

### 2.1 In-Scope Features
Testing will cover all core single-player mechanics, customization profiles and navigational layouts provided in the specification.
* **Main menu functions:** Music player (16 tracks), Help modules, and the Guided Tour system. 
* **Game configuration matrix:** 14 Decks across 3 distinct subject tracks, Grid layout variations (e.g. 1/4 (*Level 1, deck of 4 pairs*); 2/6, etc.)Geographical filters, Card back side display variations and Mode switching (time trial vs. regular).
* **Core memory engine:** Card flip responses, Top navbar helper displays, Hint (lightbulb icon) mechanics, Card (graduation cap icon) documentation and Match/Mismatch validations.
* **Accessibility & customization controls:** 
Dual age layouts (Logic puzzles for younger children in child mode vs. bonus quizzes for older children and adults), Speech speed adjustments, Volume controls, Sound toggle rules and Multi-language switches (English UK and English US).

### 2.2 Out-of-Scope Features
* **Main menu functions:** Daily brain bites, Points redemtion engine and store interfaces.
* **Multiplayer mode:** Live duals, active player matching and Network challenges are prenium-only features and are explicitly excluded from this testing phase.
* **Unverified languages:** Localization verification for the 8 non-English languages listed in the layout specifications.

---

## 3. Physical Device & Environment Matrix
Testing for this cycle is strictly restricted to the following target environment:
| Device Model | Operating system | Firmware / UI Version | Environment type |
| :--- | :--- | :--- | :--- |
| **Samsung Galaxy S21 FE 5G (Model: SM-G990E/DS / Exynos 2100)** |  Android 16 | Samsung One UI 8.0 | Local Physical Device |
Note: Virtual emulators and cloud test benches are explicitly excluded from this cycle.

---

## 4. High-level quality risks & mitigation strategies (ADHD focussed)

### RISK-01: Bright flashes and audio distortion
* **Risk:** Non-matching cards flash too brightly or audion clips distort when the volume slider is adjusted.
* **Mitigation:** Conduct manual visual audits using pre-approved UX contrast/brightness baselines to ensure animations do not strobe rapidly. Perform physical audio sweeps by manually adjusting the device volume slider from 0% to 100% across different ambient noise levels to flag audible clipping, crackling, or sudden volume spikes.

### RISK-02: Broken time trial timer
* **Risk:** The countdown time in Time Trial mode or broken state retention causes anxiety if the app is interrupted.
* **Mitigation:**  Verify state retention during minimizations so the player never loses current level progress.

### RISK-03: Advertisements cause app locks
* **Risk:** Advertisement between levels cause app locks, or the next level (up arrow) fails to load fresh randomized cards.
* **Mitigation:** Execute end-to-end flow testing specifically on the transitions between game girds, mini-games and ad wrappers.

---

## 5. Test strategy & levels of testing
Following ISTQB principles, a multi-layered testing approach will be deployed. 

### 5.1 Functional testing
- **Equivalence partitioning & BVA:** Applied rigously to the volume percentages (0 - 100%), and grid sizes (1/4, 2/6, etc.).
- **State transition testing:** Validating the flow of cards from face down, flipped/active, matched or mismatched.
### 5.2 Non-functional testing
- **Usability & accessibility testing:** Verifying the Guided Tour narration toggle works instantaneously and text does not overlap across different target devices.
- **Interruption testing:** Simulating low-battery warnings, application minimization and device locking during active matching grids.

---

## 6. Entry and Exit Criteria

### 6.1 Entry Criteria
1. The Memory Game test environment build is stabilized and deployed.
2. All functional requirements, tour scripts, and configuration specifications are finalized.
3. Test data lists for point values, regional filters, and desks are loaded into the test database.

### 6.2 Exit Criteria
1. 100% of all High-Priority test cases (Core game logic, audio sliders, and layout switches) are executed.
2. At least 95% of total test cases pass successfully.

---

## 7. Deliverables
* **Test Plan:** This document.
* **Test Case Specification:** The comprehensive test suites covering layout, play, and flow mechanics.
* **Defect Reports:** Using the structured ISTQB-compliant template for anomalies.
* **Test Summary Report:** Final metrics detailing pass/fail ratios, risk assessments, and coverage charts prior to production launch.