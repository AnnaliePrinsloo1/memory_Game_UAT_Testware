# memory_Game_UAT_Testware
An end-to-end UAT testware showcase for the Memory Game app, structured strictly according to the ISTQB Foundation Level Syllabus v4.0.1 test process.

# Memory_Game_UAT_Testware
An end-to-end UAT testware showcase for the Memory Game app, structured strictly according to the ISTQB Foundation Level Syllabus v4.0.1 test process.

# Memory Game App (Beta) - End-to-End User Acceptance Test (UAT) Run

[![ISTQB Certified](https://shields.io)](https://istqb.org)

This repository hosts the complete testware suite and execution logs for the production-readiness validation version V 20260601 of the **Memory Game App (Beta version)**. 

The primary objective of testing is to ensure a stable, calm and zero-stalls user experience. Because the application targets children, teenages and adults with ADHD, software bugs like erratic audio, sudden animation flashes or broken progression screens represent high risks fot sensory overstimulations and loss of user focus.

---

## Physical device test matrix
Testing is conducted strictly on a physical Android device.

*   **Device:** Samsung Galaxy S21 FE | Model: `SM-G990E/DS` | Android 16

---

## Test process documentation structure
The testing artifact lifecycle is divided into chronological phases to guarantee full accountability and execution traceability:

```text
├── README.md                          # Test matrix, scope, and execution summary
├── 01_Test_planning/
│   └── Memory_Game_UAT_test_plan.md   # Quality goals, device risks, entry/exit criteria
├── 02_Test_analysis/
│   └── Memory_Game_RTM.md             # RTM mapping
├── 03_Test_design/
│   └── Memory_Game_Test_cases_suite.md    # Target test cases 
├── 04_Test_implementation/
│   └── Memory_Game_Test_procedures.md     # User testing workflows
├── 05_Test_execution/
│   ├── Memory_Game_Execution_log.md   # Historical pass/fail run records
│   └── Memory_Game_Defect_report_01    # Verified bug reports
│   └── Memory_Game_Defect_report_02
│   └── Memory_Game_Defect_report_03
│   └── Memory_Game_Defect_report_04
└── 06_Test_completion/
    └── Memory_Game_Completion_report.md  # Defect density, test metrics, and release advice
```

---

## Validation methodologies & Test quality metrics

*   **Specification-Based Techniques (EP & BVA):** Applied rigorous Equivalence Partitioning (EP) and Boundary Value Analysis (BVA) to verify numerical boundaries and system configurations. This included validating point redemption tiers, custom input field limits, audio volume constraints (0–100%), and grid size configurations (ranging from 1/4 to 4/16 layout ratios) using specialized asset decks like "Colors" and "Country balls".
* **State Transition Testing:** Evaluated the behavioral logic of dynamic UI elements by tracing explicit state transitions. Tested card lifecycle states (face-down, flipped/active, and matched/mismatched pairs) alongside global application state transitions, including level progression workflows, ad-triggering intervals, and premium content lockouts.
* **Usability & Configuration Resilience:** Verified interface responsiveness, localization switching (English UK vs. English US), and visual asset scaling across multiple target device screens. Isolated critical UI bugs—such as non-linear slider scales, layout text overlaps, and freezes during the Guided Tour workflow—to ensure maximum interface stability.
* **Non-Functional & Interruption Adaptability:** Tested application resilience against real-world environment disruptions and edge-case behaviors. Evaluated game-state recovery under abrupt hardware interruptions (low-battery warnings, application minimization, and device locking) and verified input handling under simultaneous high-frequency card-tapping actions.
* **Defect Traceability & RTM:** Maintained 100% test coverage and traceability by directly mapping core store requirements down to individual functional components and defect logs (DF_001 through DF_004), establishing a clean audit trail for all observed UI and logic regressions.

---

## Active test cycle insights

*   **Total Test Scenarios Executed:** 21
*   **Total Passes:** 17
*   **Total Failures:** 4
*   **Test Pass Rate:** 80.95%
*   **Total Defects Logged:** 2 Major Issues (high severity) (DF_001, DF_003), 1 medium (DF_002) and 1 low severity (DF_004). 

---

## About the QA professional
I am an **ISTQB® Certified Freelance Software Tester** specializing in end-to-end **User Acceptance Testing (UAT)** and digital quality assurance. I partner with businesses to validate and optimize high-impact digital products before market launch, ensuring seamless user experiences and functional reliability across multiple platforms.

### Core Areas of Expertise:
*   **Mobile Application Testing:** Native Android app validation, physical device matrix testing, hardware-software interaction testing, and interruption handling.
*   **E-Commerce Platforms:** End-to-end checkout flow validation, payment gateway integration testing, shopping cart state persistence, and localized user journey verification.
*   **Web Application QA:** Cross-browser compatibility validation, responsive web design (RWD) testing, and functional regression testing.

### Let's Connect:
*   **LinkedIn:** [Annalie Prinsloo](https://www.linkedin.com/in/annalieprinsloo001/)
*   **Professional Email:** <annalieprinsloo1@gmail.com>
*   **ISTQB Verification ID:** [ZA010123GK0981040](https://scr.istqb.org/?name=Annalie+Prinsloo&number=ZA010123GK0981040&orderBy=relevancy&orderDirection=&dateStart=&dateEnd=&expiryStart=&expiryEnd=&certificationBody=&examProvider=&certificationLevel=&country=)
*   **Availability:** Open to contract, freelance QA opportunities.
