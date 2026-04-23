🌐 Wikipedia Portal - Manual QA Test Report

## Project Overview

This testing was performed on Wikipedia homepage (www.wikipedia.org) to evaluate basic functionality, usability, and stability.

The goal was simple:
	•	check how a normal user interacts with the portal
	•	identify failures, inconsistencies, or weak areas
	•	document findings in a way a developer can act on

Scope was limited to manual testing only.

## 📋 Test Coverage

| Area | TCs | Pass | Fail | Observation |
|------|-----|------|------|-------------|
| Home / Portal | 3 | 2 | 0 | 1 |
| Search | 6 | 5 | 1 | 0 |
| Navigation | 3 | 3 | 0 | 0 |
| Accessibility | 2 | 1 | 1 | 0 |
| Responsive | 2 | 2 | 0 | 0 |
| Performance | 1 | 0 | 0 | 1 |
| Error Handling | 1 | 0 | 1 | 0 |
| Security | 1 | 1 | 0 | 0 |
| Cross-Browser | 1 | 1 | 0 | 0 |
| **Total** | **20** | **15** | **3** | **2** |

---

## Key Observations
	•	Overall experience is stable and predictable
	•	Search works well for normal inputs
	•	No major crashes or blocking issues found
	•	Some edge-case handling and accessibility gaps exist
	•	Performance fluctuation noticed under slower network


## Bugs Found

BUG-01 - Search Input Handling (Edge Case)
	•	Steps:
	1.	Enter long or unusual input in search box
	2.	Use random strings or special characters
	•	Expected:
System should handle input clearly or guide the user
	•	Actual:
Results are sometimes unclear or irrelevant
	•	Impact:
Low - affects clarity, not functionality

⸻

BUG-02 - Non-existent Page Handling
	•	Steps:
	1.	Navigate to a non-existing page
	2.	Example: /wiki/RandomPage123456
	•	Expected:
Clear “Page Not Found” response
	•	Actual:
Page loads with message but behaves like a normal page
	•	Impact:
Medium - may confuse users and search engines

⸻

BUG-03 - Accessibility Issue (Search Field)
	•	Steps:
	1.	Navigate using keyboard
	2.	Use a screen reader
	•	Expected:
Search field should have a clear label
	•	Actual:
Limited or unclear context is provided
	•	Impact:
High - affects accessibility compliance

⸻

BUG-04 - Layout Shift on Slow Network
	•	Steps:
	1.	Enable slow network (3G)
	2.	Load homepage
	•	Expected:
Stable layout during loading
	•	Actual:
Content shifts after initial render
	•	Impact:
Low - minor UX issue

⸻

BUG-05 - Logo Navigation Behavior
	•	Steps:
	1.	Navigate inside the site
	2.	Click Wikipedia logo
	•	Expected:
Return to main portal
	•	Actual:
Redirects to main article page
	•	Impact:
Low - UX inconsistency

---
Detailed test cases and execution results are available in the attached Excel sheet.


## Tools Used
	•	Chrome (primary testing)
	•	Firefox (cross-browser validation)
	•	Chrome DevTools (network and performance testing)
	•	Screen reader for accessibility checks
	•	Device toolbar for responsive testing

## Tester Notes
	•	Testing focused on real-world usage scenarios
	•	Both valid and invalid inputs were tested
	•	No critical security issue confirmed
	•	Some findings may require deeper technical validation


## Conclusion

Wikipedia portal is stable and performs well under normal conditions.

Areas for improvement:
	•	Accessibility enhancements
	•	Better handling of invalid or missing pages
	•	Minor UI/UX consistency improvements
