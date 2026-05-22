# Test Analysis: User Stories & Requirements Traceability Matrix (RTM)

**Project Name:** Memory Game App Validation  
**Test Basis:** App Store Feature Specifications & User Experience Benchmarks  
**Methodology Alignment:** ISTQB® Foundation Level v4.0.1 

---

## 1. Requirements Traceability Matrix (RTM)
This Requirements Traceability Matrix (RTM) ensures 100% test coverage by directly mapping every technical requirement—derived from the Tour Features and app core objectives—to specific, manual test cases executed on the target hardware matrix.


| Req ID | Requirement Category | Requirement description | Linked Test Case (ID) | Status / Coverage |
| :--- | :--- | :--- | :--- | :--- |
| **REQ_MM_01** | Main Menu | Provide a choice of background music from a list of 16 tracks. | TC_MM_001, TC_CUST_001 | Covered |
| **REQ_MM_02** | Display a Daily Brain Bite random fact check system | TC_FLOW_001 | Covered |
| **REQ_MM_03** | Main Menu | Offer help folders containing written topic information. | TC_SET_002 | Covered |
| **REQ_MM_04** | Main Menu | Redeem points field accepting small, huge, or empty inputs. | TC_RED_001 | Covered |
| **REQ_MM_05** | Main Menu | Premium storefront for tokens, lives, and virtual coffee. | TC_FLOW_004 | Covered |
| **REQ_MM_06** | Main Menu | Outbound links for external legal docs (Privacy & EULA). | TC_MM_002 | Covered |
| **REQ_MM_07** | Main Menu | Guided app tour with an instant audio narration toggle. | TC_MM_001 | Covered |
| **REQ_GS_01** | Game Selection | Allow choice of 14 desks distributed across 3 main topics. | TC_SET_001 | Covered |
| **REQ_GS_02** | Game Selection | Configure pair counts and levels (e.g., 1/4, 2/6 grids). | TC_SET_001 | Covered |
| **REQ_GS_03** | Game Selection | Support 10 languages (including US and UK English). | TC_SET_004 | Covered |
| **REQ_GS_04** | Game Selection | Content sub-tabs for regional sorting (All, Africa, etc.). | TC_SET_002 | Covered |
| **REQ_GS_05** | Game Selection | Provide Regular mode and Time Trial game modes. | TC_SET_003 | Covered |
| **REQ_GS_06** | Game Selection | Choose card back designs to be identical or distinct. | TC_GAME_006 | Covered |
| **REQ_GS_07** | Game Selection | Info icon displaying Games-Values and Game filters text. | TC_SET_002 | Covered |
| **REQ_MP_01** | Multiplayer | Restrict multiplayer live duels to Premium tier accounts. | TTC_FLOW_004 | Covered |
| **REQ_LB_01** | Leaderboard | Show top 3 leaders per game with an expanded full view. | TC_FLOW_001 | Covered |
| **REQ_CZ_01** | Customization | Adjust narration and text speech speed via a sliding bar. | TC_CUST_001 | Covered |
| **REQ_CZ_02** | Customization | Adjust master volume levels via a smooth sliding bar. | TC_CUST_001 | Covered |
| **REQ_CZ_03** | Customization | Switch age modes (Child logic puzzles vs Adult quizzes). | TC_CUST_002 | Covered |
| **REQ_CZ_04** | Customization | Choose avatar graphics from 8 animal selection assets. | TC_MM_001 | Covered |
| **REQ_GP_01** | Gameplay | Track and duplicate active card to top-bar display layout. | TC_GAME_001 | Covered |
| **REQ_GP_02** | Gameplay | Provide a Lightbulb hint tool that briefly exposes a pair. | TC_GAME_004 | Covered |
| **REQ_GP_03** | Gameplay | Provide a Graduation cap icon revealing detailed facts of active cards. | TC_GAME_005 | Covered |
| **REQ_GP_04** | Gameplay | Matching pairs (=) vanish; support manual/auto close. | TC_GAME_002 | Covered |
| **REQ_GP_05** | Gameplay | Mismatched cards (!=) flash briefly and turn face-down. | TC_GAME_003, TC_NEG_002 | Covered |
| **REQ_GP_06** | Gameplay | Display performance metrics in a final Result Window. | TC_FLOW_001 | Covered |
| **REQ_GP_07** | Gameplay | Show ads between levels for free tier users. | TC_FLOW_003 | Covered |
| **REQ_GP_08** | Gameplay | Bottom status row showing level success by card back type. | TC_FLOW_001 | Covered |
| **REQ_GP_09** | Gameplay | Quick-action bottom controls (Replay level, Next level). | TC_FLOW_002 | Covered |
| **REQ_NF_01** | Non-Functional | App state preservation during app minimization. | TC_NEG_001 | Covered |

---

## 2. Verification metrics summary
* **Total requirements defined:** 30
* **Total requirements covered:** 30
* **Test coverage percentage:** 100%
* **Unmapped requirements:** 0
