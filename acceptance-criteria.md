# Acceptance Criteria
<!--
Acceptance criteria tell you when a user story is DONE. Each one must be testable: pass or fail.
Write 2–3 criteria for every user story using this format:

Given [a situation], when [the user does something], then [this should happen].

Tips:
- Number them under their story: AC1.1 and AC1.2 belong to US1.
- Describe what the user SEES, not how the code works.
- Include at least one "what if it goes wrong" case per story (empty input, no results).
- Avoid vague words like "fast," "nice," or "easy." Could a classmate test it and agree it passed?

Example:
## US1: View today's menu
- AC1.1: Given I open the App page, when it loads, then I see each dish with its name, photo and price.
- AC1.2: Given no dishes are added yet, when I open the menu, then I see "No dishes today yet."

AC - Acceptance Criteria
-->

### Feature: Department Treasurer Dashboard 
US1: As a user, I want to search, filter, and use a drop down list to mark student fees as Paid or Unpaid, so that I can update records quickly and avoid manual errors.
- AC1.1: Search by keyword must filter the student list immediately and be case-insensitive.
- AC1.2: Status filter must display only students matching the selected status (Paid, Pending, or Unpaid).
- AC1.3: Selecting Paid or Unpaid from the status dropdown must automatically save the change, record the date and time paid, and enable clearance approval once all required fees are settled.


### Feature: School Admin Dashboard
US2: As a user, I want to post school-wide fees and view collection metrics on the officer dashboard, so that I can oversee financial progress and ensure accurate records across all departments.
- AC2.1: Submitting a new fee form requires a Fee Description, a positive Amount (> ₱0), a Due Date, and a selected Department before assigning it as Unpaid to students in that department.
- AC2.2:  Leaving any required field blank or entering a zero/negative amount must block form submission and display an error message.
- AC2.3: The officer dashboard must display Total Expected, Total Collected, Total Unpaid, and Percentage Collected, updating dynamically when filtered by department.


### Feature: Student Dashboard 
US3: As a user, I want to view my fees and real-time clearance status on a centralized dashboard, so that I can track unpaid balances, view receipts, and check my clearance eligibility.
- AC3.1: The dashboard must display the student's profile details (Name, ID, Year/Section) and separate fees into School Fees and Department Fees tables with columns for Amount, Date Paid, Time Paid, Status, and Receipt.
- AC3.2:  Fees marked as PAID must display a green badge, exact Date/Time Paid, and a clickable View button to open the receipt, while UNPAID fees must display a red badge with blank dashes (—).
- AC3.3: The student dashboard must be strictly read-only, preventing students from editing fee amounts or changing payment statuses.


