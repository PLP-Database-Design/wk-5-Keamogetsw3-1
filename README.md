# 🧩 Assignment 5: Group Test Management — *Word Puzzle Game Plus*

## 🎯 Learning Objectives

By the end of this assignment, you will be able to:

- Develop and manage a **test plan** for a real web-based system.  
- Apply **risk-based testing** and **test prioritization** techniques.  
- Define and evaluate **entry and exit criteria**.  
- Perform **test monitoring and control** using metrics and GitHub issues.  
- Collaborate effectively in a **QA team environment**.

---

## 👥 Group Configuration

Work in **teams of exactly 3 members**.

| Role | Responsibilities |
|------|------------------|
| **Test Manager** | Draft the test plan, schedule activities, and track metrics. |
| **Risk Analyst** | Identify, assess, and prioritize risks. Design high-risk test cases. |
| **Test Executor** | Execute test cases, capture defects, and validate fixes. |

> ⚠️ **Important Group Rule:**  
> Each student must belong to **only one group**.  
> You **may not** appear in two different groups or submit under multiple teams.  
> Duplicate participation or shared submissions will be treated as **academic misconduct**.

> 💡 Collaboration via **GitHub Projects / Issues** is mandatory.  
> Each issue must include a severity level, risk mapping, and evidence (e.g., screenshot).

---

## 🕹️ System Under Test: *Word Puzzle Game Plus*

An upgraded browser-based word puzzle game that challenges players to guess scrambled words.

### 🔧 New Features (Intermediate Scope)

| Feature | Description | Test Focus |
|----------|--------------|-------------|
| **Reset Game** | Resets score and progress instantly | State management, data integrity |
| **Leaderboard** | Stores top 3 scores in `localStorage` | Persistence, boundary values |
| **Bonus Round** | Every 3 puzzles → score × 2 | Logic, arithmetic, event sequencing |

These additions increase testing complexity across functional, UI, and risk dimensions.

---

## 📋 Deliverables

All teams submit **one combined report** named `Group_Test_Management_Report.md`.

### 1️⃣ Test Plan
Include:
- Objectives  
- Scope (in/out)  
- Resources (roles + tools)  
- Schedule (phase timeline)  
- Entry / Exit criteria  
- Environment (Chrome recommended)

### 2️⃣ Risk Analysis
- Identify at least **6 risks** (functional + non-functional).  
- Rate each by **Likelihood × Impact** → Priority.  
- Define **Mitigation / Contingency** actions.  
- Add a **risk-coverage pie chart**.

---

### ✅ Test Cases

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



### 4️⃣ Defect Reporting
- Log at least **3 defects** on GitHub Issues.  
- Each issue must specify:
  - **Title**
  - **Steps to Reproduce**
  - **Expected / Actual**
  - **Severity**
  - **Risk Impact ID**
  - **Screenshot or evidence**

### 5️⃣ Test Monitoring & Metrics
Track and visualize:
- Test Case Pass %  
- Defect Density (defects / test cases)  
- Risk Coverage Ratio  
- Regression Success Rate

Represent these via tables or simple charts.

### 6️⃣ Reflection
Discuss briefly:
- How risk analysis shaped your testing focus.  
- Trade-offs between coverage, time, and depth.  
- How collaboration improved (or hindered) test effectiveness.

---

## 📊 Suggested Metrics Reference

| Metric | Formula | Example |
|---------|----------|----------|
| **Defect Density** | Defects / Test Cases |  5 / 25 = 0.2 |
| **Risk Coverage** | (Tested Risks / Total Risks) × 100 |  5 / 6 = 83 % |
| **Pass Rate** | (Passed / Total) × 100 |  18 / 20 = 90 % |

---

## 📎 Submission Checklist

✅ `Group_Test_Management_Report.md` (single file)  
✅ 3 GitHub issues (defects) linked  
✅ Screenshots / logs (optional)  
✅ Each member’s **name and role clearly stated**  
✅ One submission per group — **do not appear in multiple groups**  

> 📌 Each learner is responsible for their role’s section and must contribute equally.  
> Multiple submissions from the same student across different groups will be rejected.

---

## 🧠 Concept Reinforcement

**Risk-Based Testing Focus**  
> Prioritize based on *Risk Exposure = Probability × Impact*.

**Test Monitoring Best Practices**
- Track defects daily.  
- Update metrics at each control point.  
- Use visual indicators (tables / pie charts).

---

### 🧩 End of Assignment

Remember: Quality is measured not by the number of bugs found,  
but by how effectively your team planned, prioritized, and controlled the testing process.

Happy Testing 🧪  
