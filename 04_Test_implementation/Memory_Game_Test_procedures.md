# Test Implementation: End-to-End Test Procedures & Execution Schedule

**Project Name:** Memory Game App Validation  
**Methodology Alignment:** ISTQB® Foundation Level v4.0.1 
**Target Hardware Matrix:** Samsung Galaxy S21 FE 5G  

---

## 1. Pre-Execution Setup & Environmental Verification Checklist
### **Preconditions**
* The tester has access to the target test device (Samsung Galaxy S21 FE 5G).
* The device has a stable network connection to pull the latest beta builds.

### **Procedure**
1. Open the device settings and verify that the Google Play Beta app version accurately matches the target build release number.
2. Open the device's system tray/recent apps view and clear all background applications from the RAM.
3. Open the device system settings menu on the **S21 FE**, navigate to battery configurations, and completely disable all active battery-saver profiles.

### **Expected Results**
* The installed application build matches the staging environment requirements exactly.
* The system RAM is completely clear of background app processes to avoid performance interference.
* Battery-saving background restrictions are turned off, preventing premature background freezing or execution throttling during interruptions.

---

## 2. Test Procedures
# Test Procedures: Main Menu & Customization (Sensory & Accessibility)

## TC_MM_001: Verify Guided Tour functionality and narration toggle.

### **Preconditions**
* The app is freshly installed, or the Guided Tour is launched directly from the Main Menu.
* Device audio is turned on and set to an audible volume level.

### **Procedure**
1. Launch the application and navigate to the Main Menu.
2. Tap the **Tour** button.
3. Locate the **Speaker icon** and toggle it to the **ON** position.
4. Listen to the audio output for 5 seconds.
5. Tap the **Right Arrow** button to move to the next screen.
6. Tap the **Left Arrow** button to move back to the previous screen.
7. Toggle the **Speaker icon** to the **OFF** position.

### **Expected Results**
* The Guided Tour interface opens immediately without lag.
* Clear audio narration plays as soon as the Speaker icon is turned ON.
* Screen transitions via the navigation arrows are smooth and responsive.
* The audio narration stops immediately when the Speaker icon is toggled OFF.

---

## TC_MM_002: Verify Redirection of Legal Documents.

### **Preconditions**
* The user is currently on the Main Menu screen.
* The device has an active internet connection and a default web browser installed.

### **Procedure**
1. Tap the **Legal Docs** button on the Main Menu.
2. Tap the **Privacy Policy** option.
3. Observe the device behavior and verify the opened URL.
4. Use the device navigation to return to the application.
5. Tap the **EULA** option.
6. Verify the opened URL, then return to the application.

### **Expected Results**
* Tapping the document options safely opens the external browser.
* The URLs correctly point to the official Privacy Policy and EULA pages.
* The user can return to the application without any app crashes or state loss.

---

## TC_CUST_001: Verify Speech Speed and Sound Volume sliders.

### **Preconditions**
* The user is currently on the **Customize** settings screen.
* Device audio is enabled.

### **Procedure**
1. Drag the **Speech speed** slider all the way to the minimum value.
2. Drag the **Speech speed** slider all the way to the maximum value.
3. Drag the **Sound volume** slider to the 100% mark on the sliding bar (minimum value is 60% and maximum value is 200%).
4. Trigger an in-tour audio prompt to test the current settings.

### **Expected Results**
* Both sliders move smoothly across the bar without stuttering or freezing.
* The narration speech rate dynamically changes to match the minimum (slow) and maximum (fast) settings.
* The audio playback volume accurately reflects the 100% slider position.

---

## TC_CUST_002: Verify Age Declaration mode switching (Child vs Adult).

### **Preconditions**
* The user is currently on the **Customize** settings screen.

### **Procedure**
1. Locate the Age Declaration setting and toggle it to **Child mode**.
2. Navigate back to the game, start a match, and complete the level.
3. Return to the **Customize** screen.
4. Toggle the Age Declaration setting to **Adult mode**.
5. Return to the game, start a match, and complete the level.

### **Expected Results**
* Toggling to Child mode instantly updates the application to the Child layout.
* A child-friendly logic puzzle appears immediately after completing the level.
* Toggling to Adult mode instantly updates the application to the Adult layout.
* A mature bonus quiz appears immediately after completing the level.

---

## TC_RED_001: Boundary Value Analysis (BVA) on Point Redemption.

### **Preconditions**
* The user is currently on the **Redeem points** menu field.
* The user account has a known, valid points balance before testing.

### **Procedure**
1. Leave the code field completely empty and tap the **Redeem** button.
2. Enter a valid small integer code (e.g., 1) into the field and tap **Redeem**.
3. Enter an excessively large number (e.g., 9999999999) into the field and tap **Redeem**.

### **Expected Results**
* Leaving the field empty blocks submission and displays a clear validation error.
* Entering the small valid integer successfully processes and updates the points balance.
* Entering the excessively large number triggers a validation rejection without causing the app to crash.

---

# Test Procedures: Game Setup & Configuration

## TC_SET_001: Verify Desk and Level/Pair selection logic.

### **Preconditions**
* The user is currently on the **Game selection** screen.

### **Procedure**
1. Select one specific deck theme from the 14 options available on screen.
2. Choose a specific level/pair configuration layout (e.g., 1/4 or 2/6).
3. Tap the button to launch the game.

### **Expected Results**
* The game loads immediately using the chosen aesthetic deck theme.
* The visual grid size and layout accurately match the selected level/pair configuration.

---

## TC_SET_002: Verify Content filters (Geographic/General).

### **Preconditions**
* The user is on the **Game selection** screen, focused on the game country balls section.

### **Procedure**
1. Tap on the **Contents** tab.
2. Sequentially toggle through all filters: **All**, **Africa**, **America**, **Asia**, and **Europe**.
3. Check and note the displayed deck categories after each selection.

### **Expected Results**
* The displayed deck choices filter instantly to show only categories tied to the active region.

---

## TC_SET_003: Verify Game Mode switching (Regular vs Time Trial).

### **Preconditions**
* The user is currently on the **Game selection** screen.

### **Procedure**
1. Select the **Regular** mode option and launch the match.
2. Interact with the gameplay field, then exit back to the Game selection menu.
3. Select the **Time trial** mode option and launch the match.

### **Expected Results**
* Regular mode records cumulative turns and total time elapsed without time limits or pressure.
* Time trial mode introduces and starts a clear, highly visible countdown timer on screen.

---

## TC_SET_004: Verify Localization functionality (UK vs US English).

### **Preconditions**
* The user is inside the dedicated **Language selection** menu.

### **Procedure**
1. Choose the **English US** option and check the textual phrasing throughout the interface.
2. Choose the **English UK** option and check the textual phrasing throughout the interface.

### **Expected Results**
* UI elements dynamically change text structure based on target localization guidelines (e.g., "Color" shifts to "Colour").
* Text boxes remain aligned with no clipping, awkward overlaps, or broken UI elements.

---

# Test Procedures: Core Gameplay & Memory Mechanics

## TC_GAME_001: Verify card selection and UI helper tracking.

### **Preconditions**
* A gameplay level is launched and actively running.

### **Procedure**
1. Tap a single card facing down on the game grid.
2. Direct focus to the top navigation bar indicators.

### **Expected Results**
* The target card flips face-up without latency to display its inner icon or graphic.
* A replica of that exact card image appears clearly inside the 'Selected card' placeholder.

---

## TC_GAME_002: Verify matching pairs logic (=) and close settings.

### **Preconditions**
* A gameplay level is running, and the customization option is set to **Manual close**.

### **Procedure**
1. Find and tap two matching, identical cards in sequence on the field.
2. Keep focus on the active **Selected pair window**.
3. Tap on the layout manually to dismiss the window overview.

### **Expected Results**
* The Selected pair window displays a clear match status emblem (**=**).
* Both matched cards disappear cleanly from the active playing grid field.
* The matching alert box stays visible on screen until the user taps to dismiss it.

---

## TC_GAME_003: Verify non-matching pairs logic (!=) and card flashing.

### **Preconditions**
* A gameplay level is launched and actively running.

### **Procedure**
1. Tap two different, non-matching cards in sequence on the field.
2. Observe the active **Selected pair window** and the card grid state.

### **Expected Results**
* The Selected pair window displays a mismatch status emblem (**!=**).
* Both mismatched cards briefly flash to visually indicate the error to the user.
* The mismatched cards turn back face-down automatically in their original grid spots.

---

## TC_GAME_004: Verify Hint functionality (Lightbulb Icon).

### **Preconditions**
* A gameplay level is launched and actively running.

### **Procedure**
1. Locate and tap the **Lightbulb** hint icon residing on the top navbar.

### **Expected Results**
* The app flashes or highlights a matching card pair currently sitting on the field.
* The overall puzzle match logic and current game scoring state remain fully stable.

---

## TC_GAME_005: Verify Card Info View (Graduation cap Icon).

### **Preconditions**
* A gameplay level is launched and actively running.

### **Procedure**
1. Tap the **Graduation cap** icon on the top navbar during active gameplay.
2. Read and review the card data details presented on screen.

### **Expected Results**
* An information overlay layout slides into view showing active cards along with educational facts.

---

## TC_GAME_006: Verify Back Side icon variations (Same vs Different).

### **Preconditions**
* The game selection parameter for card backing is explicitly set to **Different** back sides.

### **Procedure**
1. Start the game match level and look closely at the face-down card designs.
2. Quit the match, go to settings, toggle the layout option to **Same** back sides, and restart.

### **Expected Results**
* In 'Different' mode, face-down cards display unique helper designs to assist in finding pairs.
* In 'Same' mode, all face-down cards feature an identical, completely uniform backing pattern.

---

# Test Procedures: End of Level & Flow Transitions

## TC_FLOW_001: Verify level completion and Result Window.

### **Preconditions**
* The user is currently in a match and flips the final matching pair left on the board.

### **Procedure**
1. Match the final pair to complete the active game level.
2. Review the final metrics rendered inside the **Result Window**.
3. Inspect the dedicated tracking layout running along the **Bottom row**.

### **Expected Results**
* The Result Window pops up displaying the finalized turn counts and clear time.
* The Bottom row updates, filling in a distinct coloured field for that completed level.

---

## TC_FLOW_002: Verify Replay and Next Level progression buttons.

### **Preconditions**
* The user has completed a level and is looking at the level **Result Window**.

### **Procedure**
1. Tap the **Replay arrow** button indicator.
2. Finish the level again, then tap on the **Up arrow** button indicator.

### **Expected Results**
* Tapping the Replay arrow restarts the level immediately with a newly randomized card deck.
* Tapping the Up arrow advances the application to the next sequential difficulty tier.

---

## TC_FLOW_003: Verify Ad appearance between levels (Free tier).

### **Preconditions**
* The active user profile is bound to the Free version tier of the mobile application.

### **Procedure**
1. Complete all matches to finish the current active game level.
2. Tap on the **Up arrow** button to progress forward.

### **Expected Results**
* A full-screen advertisement overlay displays between levels without app crashes.

---

## TC_FLOW_004: Verify Premium lockouts (Multiplayer functionality).

### **Preconditions**
* The active user profile is explicitly configured as a **Free Tier** user account.

### **Procedure**
1. Tap the **Multiplayer** icon button choice resting on the bottom navigation bar.
2. Try to initiate a live duel challenge match or online queue.

### **Expected Results**
* The multiplayer feature blocks access immediately and refuses to launch matchmaking.
* A clear subscription pop-up appears inviting the user to purchase Premium access.

---

# Test Procedures: Non-Functional & Negative Test Cases

## TC_NEG_001: Verify game state during sudden interruptions.

### **Preconditions**
* A gameplay level is launched, actively running, and the game timer is ticking.

### **Procedure**
1. Minimize the application during active play.
2. Simulate a network/system event such as an incoming phone call or native system alert.
3. Maximize and re-open the application.

### **Expected Results**
* The application restores, opening cleanly without freezing or forcing a crash.
* The countdown or elapsed timer pauses immediately at the exact second of interruption.
* The active game state layout and all uncovered card positions are perfectly preserved.

---

## TC_NEG_002: Verify simultaneous card tapping protection.

### **Preconditions**
* A gameplay level is launched and actively running.

### **Procedure**
1. Use multiple fingers to rapidly tap 3 or 4 cards simultaneously on the game grid.

### **Expected Results**
* The system safely processes only the first two inputs, ignoring additional simultaneous taps.
* The interface stays functional with no UI freezes, graphical asset overlaps, or system crashes.


