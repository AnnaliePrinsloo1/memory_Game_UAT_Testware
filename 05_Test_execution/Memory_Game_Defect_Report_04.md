## Defect Report: DF_004

* **Defect ID:** DF_004
* **Title:** Speech speed slider lacks a 100% snap-point and fine-tuning controls
* **Status:** New
* **Date Logged:** 20 May 2026
* **Reporter:** Annalie Prinsloo
* **Target Fix Version:** V 20260601

### 1. Classifications
* **Defect Type:** UI / Usability / Accessibility
* **Severity:** Low (Minor UI issue; workaround exists via meticulous manual slider manipulation)
* **Priority:** Medium (Affects accessibility customization, which is a core marketing focus of the application)
* **Reproducibility:** Systematic (Always)

### 2. Traceability & Environment
* **Associated Test Case:** TC_CUST_001
* **Hardware/Device:** Samsung Galaxy S21 FE 5G (Android 16)
* **Build Version:** Google Play Beta Build V 20260518

### 3. Description & Steps
* **Description:** The speech readback adjustments bar operates on an atypical scale spanning from 60% up to 200%. The baseline normal speed setting (100%) sits off-center within the first third of the tracking path. Because there is no default "snap-to" anchor at 100% and no incremental adjustment buttons (+/-), it is incredibly tedious for users to return to standard audio speeds.
* **Steps to Reproduce:**
  1. Open the **Customize** options screen.
  2. Tap and slide the narration sound speed control bar away from its default.
  3. Try to drag the slider thumb back precisely to the **100%** (Normal) position.
* **Expected Results:** The adjustment bar should easily snap to the 100% mark, or feature side buttons to select a baseline speed directly.
* **Actual Results:** The user must meticulously pixel-hunt along an asymmetrical scale to re-engage normal playback speed, with no fine-tuning assistance.

### 4. Evidence & Attachments
* **File Attached:** `voice-speed-slider-usability.jpg`
* **Annotation:** Screenshot shows the slider thumb resting awkwardly off-center to hit 100%, highlighting the complete lack of visual notches or adjacent +/- increment controls.
