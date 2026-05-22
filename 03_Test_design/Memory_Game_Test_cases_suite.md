# Test Design: Manual Test Cases Suite

**Project Name:** Memory Game App Validation  
**Methodology Alignment:** ISTQB® Foundation Level v4.0.1  
**Target Hardware Matrix:** Samsung Galaxy S21 FE 5G 

---

The test cases are structured to validate both standard functionality and the specific ADHD-friendly requirements (such as sensory management and low-stimulation flows).

## Test Suite 1: Main Menu & Customization (Sensory & Accessibility)
**Focus:** Ensuring the ADHD-friendly calm environment, narration, and settings function correctly.
| Test Case ID | Test Case Description | Preconditions | Test Steps | Expected Result | Priority |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_MM_001** | Verify Guided Tour functionality and narration toggle. | App is freshly installed or Tour is launched from Main Menu. | <ol><li>Click 'Tour' from Main Menu.</li><li>Toggle the Speaker icon ON.</li><li>Navigate through the tour screens using the left/right arrows</li><li>Toggle the Speaker icon OFF.</li></ol> | <ol><li>Guided tour opens successfully.</li><li>Audio narration plays when ON.</li><li>Arrows navigate screens smoothly.</li><li>Narration stops instantly when toggled OFF.</li></ol> | High |
| **TC_MM_002** | Verify Redirection of Legal Documents. | User is on the Main Menu screen. | <ol><li>Tap on 'Legal Docs'.</li><li>Select 'Privacy Policy'.</li><li>Return to app and select 'EULA'.</li></ol> | <ol><li>Browser/external link opens safely with correct URL.</li><li>User can seamlessly return to the app.</li></ol> | Medium |
| **TC_CUST_001** | Verify Speech Speed and Sound Volume sliders. | User is on the 'Customize' screen. | <ol><li>Adjust the 'Speech speed' slider to minimum, then maximum.</li><li>Adjust the 'Sound volume' slider via the sliding bar.</li><li>Test an in-tour audio prompt.</li></ol> | <ol><li>Sliders move smoothly without freezing.</li><li>Speech rate changes dynamically (slower/faster).</li><li>Volume matches slider position.</li></ol> | High |
| **TC_CUST_002** | Verify Age Declaration mode switching (Child vs Adult). | User is on the 'Customize' screen. | <ol><li>Toggle Age Declaration to 'Child mode'.</li><li>Complete a game level.</li><li>Change Age Declaration to 'Adult mode'.</li><li>Complete a game level.</li></ol> | <ol><li>App switches to Child mode layout.</li><li>Logic puzzles appear between levels.</li><li>App switches to Adult mode layout.</li><li>Bonus quiz appears between levels.</li></ol> | High |
| **TC_RED_001** | Boundary Value Analysis (BVA) on Point Redemption. | User is on 'Redeem points' menu field. | <ol><li>Leave code field empty and click Redeem.</li><li>Enter a small valid integer.</li><li>Enter an excessively large number (e.g., 9999999999).</li></ol> | <ol><li>System throws a clear validation error.</li><li>Points are redeemed successfully.</li><li>System rejects input without crashing.</li></ol> | Medium |

## Test Suite 2: Game Setup & Configuration 
**Focus:** Validating game parameters, language selection, and content filters.
| Test Case ID | Test Case Description | Preconditions | Test Steps | Expected Result | Priority |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_SET_001** | Verify Desk and Level/Pair selection logic. | User is on the 'Game selection' screen. | <ol><li>Select a deck from the 14 options.</li><li>Select a level/pair configuration (e.g., 1/4 or 2/6).</li><li>Launch the game.</li></ol> | <ol><li>Game loads with the chosen desk theme.</li><li>Grid size correctly matches the selected level/pair parameters.</li></ol> | High |
| **TC_SET_002** | Verify Content filters (Geographic/General). | User is on the 'Game selection' screen on the game country balls. | <ol><li>Tap the 'Contents' tab.</li><li>Toggle through filters: All, Africa, America, Asia, Europe.</li><li>Verify the displayed desk categories.</li></ol> | <ol><li>Content filters correctly isolate desks associated with that specific region/topic.</li></ol> | Medium |
| **TC_SET_003** | Verify Game Mode switching (Regular vs Time Trial). | User is on the 'Game selection' screen. | <ol><li>Select 'Regular' mode and start game.</li><li>Exit, select 'Time trial' mode and start game.</li></ol> | <ol><li>Regular mode tracks turns/time without pressure limits.</li><li>Time trial introduces a visible countdown timer.</li></ol> | High |
| **TC_SET_004** | Verify Localization functionality (UK vs US English). | User is on the Language selection menu.User is on the Language selection menu. | <ol><li>Select 'English US' and verify game text.</li><li>Select 'English UK' and verify game text.</li></ol> | <ol><li>Text localizes correctly (e.g., 'Color' vs 'Colour').</li><li>No overlapping text or UI breaking occurs.</li></ol> | Low |

## Test Suite 3: Core Gameplay & Memory Mechanics
**Focus:** Testing card behaviour, matching logic, and cognitive assist tools.
| Test Case ID | Test Case Description | Preconditions | Test Steps | Expected Result | Priority |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_GAME_001** | Verify card selection and UI helper tracking. | Game level is launched. | <ol><li>Tap on a single card.</li><li>Observe the top navigation bar.</li></ol> | <ol><li>Card flips to reveal content.</li><li>Card image duplicates cleanly into the 'Selected card' placeholder window.</li></ol> | High |
| **TC_GAME_002** | Verify matching pairs logic (=) and close settings. | Game level is launched. Customization set to 'Manual close'. | <ol><li>Select two identical/matching cards.</li><li>Observe the 'Selected pair window'.</li><li>Tap to manually close/dismiss.</li></ol> | <ol><li>Pair window shows match (=) status.</li><li>Cards disappear from field.</li><li>Cards remain cleared according to manual setting.</li></ol> | High |
| **TC_GAME_003** | Verify non-matching pairs logic (!=) and card flashing. | Game level is launched. | <ol><li>Select two different cards.</li><li>Observe the 'Selected pair window' and card grid.</li></ol> | <ol><li>Window shows mismatch (!=) status.</li><li>Non-matching cards briefly flash visually.</li><li>Cards return face-down to original positions.</li></ol> | High |
| **TC_GAME_004** | Verify Hint functionality (Lightbulb Icon). | Game level is actively running. | <ol><li>Tap the 'Lightbulb' icon in the top navbar.</li></ol> | <ol><li>App briefly flashes/reveals a matching pair on the field.</li><li>Game state remains stable.</li></ol> | Medium |
| **TC_GAME_005** | Verify Card Info View (Graduation cap Icon). | Game level is actively running. | <ol><li>Tap the 'Graduation cap' icon in the top navbar during gameplay.</li><li>Review card details.</li></ol> | <ol><li>Opens an overlay showing the cards in play with additional educational facts.</li></ol> | Medium |
| **TC_GAME_006** | Verify Back Side icon variations (Same vs Different). | Game selection set to 'Different' back sides. | <ol><li>Start a game level.</li><li>Observe the face-down card designs.</li><li>Restart with 'Same' back sides setting.</li></ol> | <ol><li>Face-down cards display unique helper icons for pairs.</li><li>Face-down cards display uniform identical icons.</li></ol> | High |

## Test Suite 4: End of Level & Flow Transitions
**Focus:** Post-game rewards, mini-games, progression, and ad integration.
| Test Case ID | Test Case Description | Preconditions | Test Steps | Expected Result | Priority |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_FLOW_001** | Verify level completion and Result Window. | User matches the final pair on the board. | <ol><li>Complete the level.</li><li>Observe metrics in the Result Window.</li><li>Verify the 'Bottom row' level tracking.</li></ol> | <ol><li>Result window appears with turn counts and clear time.</li><li>Bottom row updates with a coloured field for completed levels.</li></ol> | High |
| **TC_FLOW_002** | Verify Replay and Next Level progression buttons. | User is on the level Result Window. | <ol><li>Tap the 'Replay arrow'.</li><li>Complete level again, then tap the 'Up arrow'.</li></ol> | <ol><li>Replay arrow restarts the level with a newly randomized deck.</li><li>Up arrow safely advances to the next difficulty level.</li></ol> | High |
| **TC_FLOW_003** | Verify Ad appearance between levels (Free tier). | User is using the free version of the app. | <ol><li>Complete a game level.</li><li>Tap 'Up arrow' to progress.</li></ol> | <ol><li>An advertisement overlay safely appears between levels without crashing the app.</li></ol> | Medium |
| **TC_FLOW_004** | Verify Premium lockouts (Multiplayer functionality). | User profile is Free Tier (Non-Premium). | <ol><li>From bottom nav bar, tap 'Multiplayer'.</li><li>Attempt to start a live duel or challenge.</li></ol> | <ol><li>Feature is blocked.</li><li>User is presented with a clear upgrade path/Premium subscription window.</li></ol> | High |

## Non-Functional & Negative Test Cases
**Focus:** Verifying stress handling, security boundaries, and validation errors.
| Test Case ID | Test Case Description | Preconditions | Test Steps | Expected Result | Priority |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_NEG_001** | Verify game state during sudden interruptions. | Game level is actively running. | <ol><li>Minimize app during active play.</li><li>Simulate an incoming phone call.</li><li>Re-open/maximize the app.</li></ol> | <ol><li>App recovers cleanly.</li><li>Timer pauses instantly on interruption.</li><li>Game state and uncovered positions are perfectly preserved.</li></ol> | High |
| **TC_NEG_002** | Verify simultaneous card tapping protection. | Game level is actively running. | <ol><li>Rapidly tap 3 or 4 cards simultaneously with multiple fingers.</li></ol> | <ol><li>System processes only the first two inputs cleanly.</li><li>App UI does not freeze, overlap images, or crash.</li></ol> | Medium |