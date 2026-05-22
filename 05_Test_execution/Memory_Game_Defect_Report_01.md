## Defect Report: DF_001

* **Defect ID:** DF_001
* **Title:** App hangs on 7th Tour screen during long load sequence
* **Status:** New
* **Date Logged:** 20 May 2026
* **Reporter:** Annalie Prinsloo
* **Target Fix Version:** V 20260601

### 1. Classifications
* **Defect Type:** Functional / Performance (Crash/Hang)
* **Severity:** High (System core functionality is severely degraded; UI hangs)
* **Priority:** Medium (Urgency is lowered slightly because reproducibility is "Sometimes")
* **Reproducibility:** Intermittent (Sometimes)

### 2. Traceability & Environment
* **Associated Test Case:** TC_MM_001
* **Hardware/Device:** Samsung Galaxy S21 FE 5G (Android 16)
* **Build Version:** Google Play Beta Build V 20260518

### 3. Description & Steps
* **Description:** While connected to a stable internet connection, navigating to the 7th tour screen triggers an excessively long loading phase. During this period, the entire user interface completely freezes, causing the Exit ("X") button to become entirely unresponsive and trapping the user inside the tour view. This represents a significant risk for the target ADHD demographic due to lack of visual feedback during hangs.
* **Steps to Reproduce:**
  1. Navigate to the main menu icon and tap it.
  2. Select the **Tour** option from the menu list.
  3. Tap the forward navigation arrow (right side) 6 times sequentially to reach the 7th tour screen.
  4. Attempt to tap the "X" exit button located in the tour window overlay.
* **Expected Results:** The 7th tour screen should load quickly (< 2 seconds), and tapping the "X" button should instantly close the tour overlay and return the user safely to the main menu.
* **Actual Results:** The 7th tour screen triggers an indefinite loading loop. The main UI thread completely freezes, rendering the "X" button unresponsive and forcing a hard application termination.

### 4. Evidence & Attachments
* **File Attached:** `7th-tour-screen-ui-freeze.mp4`
* **URL:** https://youtu.be/smQAPJcSf4A
* **Annotation:** Video showcases smooth navigation through screens 1–6, followed by a total thread lock on screen 7. Multiple tap attempts on the "X" button fail completely at timestamp 6:32.