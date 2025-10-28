#  Group Test Management Report — Word Puzzle Game Plus

---

## 1 TEST PLAN

### a) Objectives
To test all new and existing features of **Word Puzzle Game Plus**, focusing on reset, leaderboard, and bonus logic.

---

### b) Scope
**In-Scope:** Functional testing, UI, risk-based testing.  
**Out-of-Scope:** Backend/server testing (not applicable, uses localStorage).

---

### c) Resources

| Role | Member | Tools |
|------|---------|-------|
| Test Manager | keamogetswe | GitHub Projects, Docs |
| Risk Analyst | justine | Excel, GitHub |
| Test Executor | Sally | Chrome, Screenshots, GitHub Issues |

---

### d) Schedule

| Phase | Dates |
|-------|-------|
| Planning | Oct 27 |
| Risk Analysis | Oct 27 |
| Test Design | Oct 27 |
| Execution | Oct 27 |
| Reporting | Oct 27 |

---

### e) Entry Criteria
- Game loads successfully on Chrome.  
- Team roles assigned.  
- Test cases approved.

---

### f) Exit Criteria
- All planned test cases executed.  
- Critical defects closed or deferred.  
- Metrics compiled and reviewed.

---

##  STEP 4 — Conduct Risk Analysis (by Risk Analyst)

Identify at least 6 risks and rate them Likelihood × Impact = Priority.

| ID | Risk | Likelihood | Impact | Priority | Mitigation |
|----|------|-------------|---------|-----------|-------------|
| R1 | Leaderboard not saving | 5 | 5 | 25 (High) | Test storage thoroughly |
| R2 | Reset doesn’t clear state | 4 | 5 | 20 (High) | Include mid-play reset test |
| R3 | Bonus round miscalculates | 3 | 4 | 12 (Medium) | Test event sequence |
| R4 | UI not responsive | 2 | 3 | 6 (Low) | Usability test |
| R5 | Score overflow | 3 | 3 | 9 (Medium) | Boundary testing |
| R6 | Browser storage full | 2 | 4 | 8 (Medium) | Validate localStorage handling |

---

## Test Design & Execution

**ID: TC-01**  
**Feature:** Reset Game  
**Objective:** Verify that the “Reset” button clears score and progress.  
**Steps:**  
1. Play and solve at least 1 puzzle.  
2. Click the “Reset” button.  
**Expected:** Score resets to 0, solved puzzles reset to 0, leaderboard remains unchanged.  
**Risk Priority:** High  

---

**ID: TC-02**  
**Feature:** Reset Game  
**Objective:** Ensure leaderboard data remains after reset.  
**Steps:**  
1. Achieve a score high enough to appear on the leaderboard.  
2. Click “Reset.”  
**Expected:** Leaderboard still displays top 3 scores.  
**Risk Priority:** Medium  

---

**ID: TC-03**  
**Feature:** Leaderboard  
**Objective:** Verify top-3 sorting logic.  
**Steps:**  
1. Achieve scores 5, 12, 8.  
2. Open leaderboard.  
**Expected:** Scores displayed in descending order (12, 8, 5).  
**Risk Priority:** High  

---

**ID: TC-04**  
**Feature:** Leaderboard  
**Objective:** Verify leaderboard saves to localStorage.  
**Steps:**  
1. Achieve a top score.  
2. Refresh the browser.  
**Expected:** Leaderboard retains previous top 3 scores.  
**Risk Priority:** High  

---

**ID: TC-05**  
**Feature:** Bonus Round  
**Objective:** Confirm that the score doubles every 3 solved puzzles.  
**Steps:**  
1. Solve 3 puzzles correctly.  
2. Observe score calculation.  
**Expected:** Score is multiplied by 2.  
**Risk Priority:** High  

---

**ID: TC-06 (Negative Test)**  
**Feature:** Hint System  
**Objective:** Verify penalty when using a hint.  
**Steps:**  
1. Use “Hint.”  
2. Solve the puzzle.  
**Expected:** -2 points deducted and +5 points added (total +3).  
**Risk Priority:** Medium  

---

**ID: TC-07 (Negative Test)**  
**Feature:** Guess Validation  
**Objective:** Ensure invalid guesses are rejected.  
**Steps:**  
1. Enter a random word not matching the scrambled word.  
2. Click “Submit.”  
**Expected:** Message like “Incorrect! Try again” appears; score does not increase.  
**Risk Priority:** Medium  

---

**ID: TC-08 (Usability Test)**  
**Feature:** UI Layout and Controls  
**Objective:** Check that all buttons (Submit, Hint, New Puzzle, Reset) are visible and clickable.  
**Steps:**  
1. Open the game on Chrome (desktop).  
2. Observe and interact with all buttons.  
**Expected:** All buttons function as intended, with proper spacing and labels.  
**Risk Priority:** Low  

---
---

## STEP 5 — Defect Reporting (by Test Executor)

Each defect was logged on **GitHub Issues** with severity, risk mapping, and evidence (screenshots attached in the repository).

| ID | Title | Steps to Reproduce | Expected Result | Actual Result | Severity | Risk Impact | Evidence |
|----|--------|--------------------|------------------|----------------|-----------|--------------|-----------|
| D1 | Leaderboard not saving after refresh | 1. Play and achieve a high score.<br>2. Refresh the page.<br>3. Check leaderboard. | Score should persist in localStorage. | Leaderboard clears on refresh. | High | High | Screenshot: `leaderboard_bug.png` |
| D2 | Reset button not clearing bonus points | 1. Solve 3 puzzles to activate bonus round.<br>2. Click Reset.<br>3. Observe score. | All scores and bonuses reset to 0. | Bonus points remain visible. | Medium | Medium | Screenshot: `reset_bug.png` |
| D3 | UI buttons misaligned on small screens | 1. Open game on Chrome mobile view.<br>2. Observe layout. | Buttons aligned and accessible. | Buttons overlap on smaller screen sizes. | Low | Low | Screenshot: `ui_bug.png` |

---

###  GitHub Issues Summary
All defects are tracked in the **GitHub Issues** tab under this repository.  
Each issue includes:
- Severity level (High / Medium / Low)  
- Risk mapping  
- Screenshot or video evidence  
- Steps to reproduce  
- Fix validation status (Open, Fixed, Retested)

---

### Example GitHub Issue Format
**Title:** Leaderboard not saving after refresh  
**Steps to Reproduce:**
1. Play and achieve a high score.  
2. Refresh the page.  
3. Open the leaderboard.  
**Expected:** Score persists via localStorage.  
**Actual:** Leaderboard clears.  
**Severity:** High  
**Risk Impact:** High  
**Evidence:** Attached screenshot `leaderboard_bug.png`  
**Status:** Open  

---
---

## STEP 6 — Test Monitoring & Metrics (by Test Manager)

This section tracks testing progress using key QA metrics such as Pass Rate, Defect Density, Risk Coverage, and Regression Success Rate.

---

### Test Summary Table

| Metric | Formula | Example Calculation | Result |
|--------|----------|----------------------|---------|
| **Pass Rate** | (Passed / Total) × 100 | (7 / 8) × 100 | **87.5%** |
| **Defect Density** | Defects / Test Cases | 3 / 8 | **0.375** |
| **Risk Coverage** | (Tested Risks / Total Risks) × 100 | (5 / 6) × 100 | **83%** |
| **Regression Success Rate** | (Successful Retests / Total Retests) × 100 | (2 / 3) × 100 | **66.7%** |

---

###  Visualization Summary

####  Test Case Pass %
| Status | Count | Percentage |
|--------|--------|-------------|
| Passed | 7 | 87.5% |
| Failed | 1 | 12.5% |

####  Defect Density
- **Total Test Cases:** 8  
- **Total Defects Found:** 3  
- **Defect Density:** 0.375  

#### Risk Coverage Ratio
- **Total Risks Identified:** 6  
- **Risks Tested:** 5  
- **Coverage:** 83%  

####  Regression Success Rate
- **Total Retests:** 3  
- **Successful Retests:** 2  
- **Rate:** 66.7%

---

### Key Observations
- Most functional areas passed initial testing.  
- The **Leaderboard** feature presented the highest risk and defect count.  
- **UI responsiveness** issues were minor and marked as *Low* severity.  
- Risk-based prioritization ensured focus on *bonus and leaderboard logic*, which had the highest impact on gameplay.

---

###  Reflection

####  How risk analysis shaped testing focus:
The team concentrated test efforts on high-risk areas — particularly the leaderboard persistence and bonus logic — which were most likely to impact user experience and scoring accuracy.

####  Trade-offs between coverage, time, and depth:
Limited testing time meant deprioritizing some low-risk UI cases in favor of deeper functional testing on the scoring and reset mechanisms.

#### Collaboration effectiveness:
Using **GitHub Projects and Issues** improved task coordination, ensuring clear ownership and faster defect tracking. However, asynchronous communication sometimes caused duplicate test executions.

---
**End of Report**

Each member contributed equally:
- **Test Manager:** (Name) — Planning, Metrics, Report Compilation  
- **Risk Analyst:** (Name) — Risk Identification, Prioritization  
- **Test Executor:** Sally — Test Execution, Defect Logging

---

