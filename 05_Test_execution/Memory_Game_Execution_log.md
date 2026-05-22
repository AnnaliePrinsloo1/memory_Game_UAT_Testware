# Test Execution Log: Memory Game (Beta)

## 1. General Metadata
* **Document ID:** EL_Memory_Game_01
* **Date of Execution:** 20 May 2026
* **Executed By:** Annalie Prinsloo
* **Test Cycle:** Beta Sprint 1 - Accessibility & Core Flow
* **Test Environment:** 
  * **Device:** Samsung Galaxy S21 FE 5G (Model: SM-G990B)
  * **OS Version:** Android 16 (One UI 8.0)
  * **App Version:** Google Play Beta Build V 20260518
  * **Network Profile:** Stable Wi-Fi (Symmetrical 100Mbps) / Cellular 5G

## 2. Summary Metrics
* **Total Test Cases Planned:** 21
* **Total Test Cases Executed:** 21
* **Passed:** 17
* **Failed:** 4 (TC_MM_001, TC_CUST_001, TC_CUST_002, TC_FLOW_003 scored as Fail due to active defects)
* **Blocked:** 0

## 3. Execution Results Table

| Test Case ID | Test Suite / Focus | Status | Linked Defect ID | Remarks / Observations |
| :--- | :--- | :--- | :--- | :--- |
| **TC_MM_001** | Main Menu: Guided Tour | **FAIL** | DF_001, DF_002 | UI freezes on screen. False offline banner appears. |
| **TC_MM_002** | Main Menu: Legal Docs | **PASS** | None | Redirection to browser is smooth and returns cleanly. |
| **TC_CUST_001** | Customization: Sliders | **FAIL** | DF_004 (UI) | Code blocked out-of-bounds inputs. Slider scale is non-linear. |
| **TC_CUST_002** | Customization: Age Mode | **FAIL** | DF_003 | Logic puzzles displayed in child mode and bonus quiz appears in adult mode verified. Logic puzzle does not advance. |
| **TC_RED_001** | Redeem points: BVA | **PASS** | None | System throws validation errors where expected. |
| **TC_SET_001** | Setup: Grid Configuration | **PASS** | None | Verified using "Colors" deck at 1/4, 2/6, 3/8 & 4/16 layout ratios. |
| **TC_SET_002** | Setup: Content Filters | **PASS** | None | Verified using "Country balls" filter configuration. |
| **TC_SET_003** | Setup: Game Modes | **PASS** | None | Verified using Regular mode tracking. |
| **TC_SET_004** | Setup: User Language | **PASS** | None | Verified switching between English UK and English US. |
| **TC_GAME_001** | Gameplay: Card selection | **PASS** | None | Card selection and UI helper tracking verfied. |
| **TC_GAME_002** | Gameplay: Card matching pairs | **PASS** | None | Card logic matching verfied. |
| **TC_GAME_003** | Gameplay: Card non-matching pairs | **PASS** | None | Card logic non-matching verfied. |
| **TC_GAME_004** | Gameplay: Card hint | **PASS** | None | Flashing matching cards hint verfied. |
| **TC_GAME_005** | Gameplay: Game information | **PASS** | None | Graduation cap displays which pairs match verified. |
| **TC_GAME_006** | Gameplay: Card Backs | **PASS** | None | Validated uniform Same back vs. different back sides. |
| **TC_FLOW_001** | Flow transitions: Level completion and results window | **PASS** | None | Validated that results window appear correctly after game level is completed. |
| **TC_FLOW_002** | Flow transitions: Replay and next level progression | **PASS** | None | Validated replay and next level progression functions correctly. |
| **TC_FLOW_003** | Flow transitions: Ad appearance | **FAIL** | DF_002 | Ads do appear but false offline warning banner also appears simultaneously. |
| **TC_FLOW_004** | Flow transitions: Premium lockout | **PASS** | None | Verified premium lockout blocked. |
| **TC_NEG_001** | Non-functional: Game state interruption | **PASS** | None | Verified that game state recovers correctly. |
| **TC_NEG_002** | Non-functional: Simultaneous card tapping | **PASS** | None | Verified that only first two inputs are processed. |