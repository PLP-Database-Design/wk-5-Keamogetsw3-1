# 🧪Final Group Test Report — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management  
**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28  

---

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| Test Manager | Keamogetswe M | Planning, scheduling, coordination, metric tracking |
| Risk Analyst | Sally Trizer | Risk identification, prioritization, test design linkage |
| Test Executor | Martin Justine | Execution, evidence capture, defect logging |

---

## Group Rules

- Each student must belong to only one group.  
- Duplicate membership or multiple submissions will result in invalidation.  
- Every group member must contribute towards this project.  

---

##  Project Overview

**System Under Test:** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Environment:** Chrome Browser (Desktop)

### Features Under Test

| Feature | Description | Risk Category |
|---------|-------------|---------------|
| Reset Game | Clears score and progress instantly | High |
| Leaderboard | Stores top 3 scores in localStorage | High |
| Bonus Round | Every 3 puzzles → doubles score | High |

---

## 🧭 Test Plan

### Objectives

- The objective of this test plan is to validate the following:
  - Clicking 'reset' sets score = 0 and clears progress
  - Leaderboard accuracy and localStorage behaviour
  - Bonus round triggers correctly and applies score multipliers

### Scope

**In Scope:**
- Reset Game score and progress  
- Leaderboard functionality and localStorage  
- Bonus round score calculation   

**Out of Scope:**
- Server-side or backend testing (local-only)  
- Mobile browser compatibility  

---

###  Tools & Resources

| Tool / Resource | Purpose |
|-----------------|----------|
| Google Chrome | Test execution environment |
| GitHub Issues | Defect tracking and logginf |
| WhatsApp Messenger | Team communication |

---

### ⏱️ Schedule

| Phase | Planned Duration | Actual Duration | Status |
|-------|------------------|-----------------|--------|
| Test Planning | 4 hours | 2 hours | Completed |
| Risk Analysis | 3 hours | 2 hours | Completed |
| Test Design | 4 hours | 3 hours | Completed |
| Test Execution | 5 hours | 4 hours | Completed |
| Reporting | 3 hours | 2 hours | Completed |

---

##  Risk Analysis

### Identified Risks

| ID | Feature | Risk Description | Likelihood | Impact | Priority | Mitigation Strategy |
|----|----------|------------------|------------|---------|-----------|---------------------|
| R1 | Leaderboard | Scores not saving correctly | 5 | 5 | 25 (High) | Verify localStorage save/load |
| R2 | Reset Game | Game not resetting mid-play | 4 | 5 | 20 (High) | Test reset during active game |
| R3 | Bonus Round | Score not doubling after 3 puzzles | 3 | 4 | 12 (Medium) | Simulate multiple rounds |
| R4 | UI Layout | Buttons overlap or missing | 2 | 3 | 6 (Low) | Usability test on Chrome |
| R5 | Hint System | Hint penalty miscalculated | 3 | 3 | 9 (Medium) | Negative test case |
| R6 | Storage Limit | LocalStorage full | 2 | 4 | 8 (Medium) | Validate save error handling |

### Risk Coverage

- **Tested Risks Percent:** 100%  
- **Untested Risks Percent:** 0%

---

## Test Cases

| ID | Feature | Objective | Expected Result | Actual Result | Status | Risk Link |
|----|----------|-----------|----------------|---------------|--------|-----------|
| TC-01 | Reset Game | Verify reset clears score | Score resets to 0 | Works correctly | Pass | R2 |
| TC-02 | Reset Game | Ensure leaderboard remains after reset | Leaderboard unchanged | Works correctly | Pass | R1 |
| TC-03 | Leaderboard | Verify sorting logic | Sorted descending | Works | Pass | R1 |
| TC-04 | Leaderboard | Data persists after refresh | Data retained | Works | Pass | R1 |
| TC-05 | Bonus Round | Double score every 3 puzzles | Score doubled | works | Pass | R3 |
| TC-06 | Hint System | Verify penalty applied | -2 +5 total +3 | Works | Pass | R5 |
| TC-07 | Guess Validation | Reject invalid guesses | “Incorrect” message displayed | Works | Pass | R5 |
| TC-08 | UI Layout | Buttons visible and clickable | All clickable and visible | Works | Pass | R4 |

---

##  Defects Logged

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|--------------|----------|----------|--------|-------------|
| D01 | Refresh Button does not reset the leadership| Medium | R3 | Open | [GitHub Issue #5](https://github.com/PLP-Database-Design/wk-5-Keamogetsw3-1/issues/4) |
| D02 | Hint button penalty delay | Medium | R5 | Closed | [GitHub Issue #7](https://github.com/) |

---

##  Metrics

- **Test Case Pass Percent:** 87.5% (7/8 passed)  
- **Defect Density:** 0.25 (2 defects / 8 test cases)  
- **Risk Coverage Percent:** 100% (6/6 tested)  
- **Regression Success Rate:** 90%  

### Defect Summary

- **Total Defects Logged:** 2  
- **Critical / High Severity:** 1  
- **Fix Rate:** 50%

---

## Test Control & Project Management

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|-------------|---------------|----------|-------|
| Planning | Test Plan | Completed | 0% | Keamogetswe M |
| Risk Analysis | Risk Matrix | Completed | 0% | Sally Trizer |
| Execution | Test Evidence | Completed | 0% | Faith N |
| Reporting | Final Report | Completed | 0% | All Members |

**Progress Tracking Method:** GitHub Issues and WhatsApp  
**Change Control Notes:** All major changes discussed on group chat before update  

---

## Lessons Learned

- **Most Defect Prone Feature:** Bonus Round  
- **Risk Analysis Impact:** Helped focus testing on high-priority risks  
- **Team Communication:** Effective — quick coordination on WhatsApp  
- **Improvements for Next Cycle:** Earlier risk identification and partial automation testing  

---

## Attachments / Evidence

- Screenshot 1: Leaderboard sorting result  
- Screenshot 2: Reset button functionality  
- Screenshot 3: Bonus  calculation issue  

## Sign Off
| Name              | Role            | Initials | Date |
|-------------------|-----------------|-----------|------|
|  Keamogetswe    | Test Manager |    K       |    28/1012025  |
|   Justin   | Risk Analyst    |       J    |    28/10/2025  |
|    Sally  | Test Executor              |      S     |   28/10/2025   |

		
## Overall Summary
### Statement:

Test Status: ☐ Completed / ☐ In Progress / ☐ Deferred

