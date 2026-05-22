## Defect Report: DF_002

* **Defect ID:** DF_002
* **Title:** False "Looks like you’re offline" warning banner triggers during active gameplay
* **Status:** New
* **Date Logged:** 20 May 2026
* **Reporter:** Annalie Prinsloo
* **Target Fix Version:** V 20260601

### 1. Classifications
* **Defect Type:** UI / Usability
* **Severity:** Medium (System remains functional, but displays incorrect/misleading information to the user)
* **Priority:** High (High business urgency as it impacts core gameplay screens and presents a chaotic sensory experience for ADHD users)
* **Reproducibility:** Intermittent (Sometimes)

### 2. Traceability & Environment
* **Associated Test Case:** TC_MM_001 / TC_FLOW_003
* **Hardware/Device:** Samsung Galaxy S21 FE 5G (Android 16)
* **Build Version:** Google Play Beta Build V 20260518

### 3. Description & Steps
* **Description:** During active gameplay and tour navigation, an error message reading *"Looks like you’re offline. No worries, but keep in mind some features need the internet. Want to play anytime?"* erroneously displays across the bottom layout. This occurs despite a fully active, stable web connection, verified by successful concurrent third-party ad serving.
* **Steps to Reproduce:**
  1. Open the application, go to the Game Selection area, and tap it.
  2. Apply the following options: Deck: *Colors*, Layout: *1/4*, Filter: *Shapes*, Mode: *Regular*, Backing: *Same*.
  3. Press the **Play** button.
  4. Dismiss the game information modal by tapping the "X" icon.
  5. Flip game cards to initiate active matching rounds and observe the bottom UI region.
* **Expected Results:** The puzzle match session proceeds with zero connectivity warnings if a stable network link is present.
* **Actual Results:** A false "Looks like you're offline..." notification banner pushes onto the screen layout and remains dynamically stuck, despite live ads successfully rendering underneath.

### 4. Evidence & Attachments
* **File Attached:** `Offline-Banner-Bug-Gameplay.mp4`
* **URL:** https://youtube.com/shorts/Xaous0lJ9rs?feature=share
* **Annotation:** Clip showcases active card interactions using the "Colors" set while a persistent network error message remains stuck on screen despite live third-party ads successfully rendering.