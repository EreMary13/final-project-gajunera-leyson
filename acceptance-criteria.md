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

US1: As a Department Treasurer, I want to search, filter, and use a dropdown to update a student's fee status to Paid or Unpaid so that payment records stay accurate without manual errors.
- AC1.1: Typing a keyword in the search box filters the student list immediately and is case-insensitive.
- AC1.2: Selecting Paid or Unpaid in the status filter displays only students matching that status (plus an option to show all students).
- AC1.3: Selecting Paid or Unpaid from the fee status dropdown automatically saves the change to localStorage, records the date and time paid when marked Paid (or resets them to — when switched back to Unpaid), and updates clearance status automatically in real time once all required fees are Paid.

US2: As a Department Treasurer, I want to post department-specific or year-level fees so that students in my assigned group are billed for their required fees.
- AC2.1: Submitting the new fee form requires a Fee Description, a positive Amount (> ₱0), a Due Date, and a target department/year-level group before adding the fee as Unpaid for students in that group.
- AC2.2: Leaving any required field blank or entering 0 or a negative amount blocks submission and displays a clear error message.

US3: As a Department Treasurer, I want to view the student clearance list with real-time clearance statuses so that I can verify which students are automatically cleared once all required fees are Paid.
- AC3.1: Each student's clearance status automatically displays Cleared when all of their required fees are Paid, and displays Not Cleared if any required fee remains Unpaid.

### Feature: School Admin Dashboard

US1: As a School Admin, I want to post school-wide fees for all departments so that campus-wide obligations apply to every student.
- AC1.1: Submitting the school-wide fee form requires a Fee Description, a positive Amount (> ₱0), a Due Date, and All Departments selected before recording the fee as Unpaid across all departments and students.
- AC1.2: Leaving any required field blank, entering 0 or a negative amount, or selecting a single department instead of All Departments blocks submission and displays a clear error message.

US2: As a School Admin, I want to view collection metrics, student counts, and financial statistics on the officer dashboard so that I can monitor financial progress across the school.
- AC2.1: The officer dashboard displays Total Expected, Total Collected, Total Unpaid, Percentage Collected, and student counts calculated from current fee records.

US3: As a School Admin, I want to filter collection metrics, student counts, and posted fees by department or institute so that I can check records for a specific unit.
- AC3.1: Selecting a department or institute from the filter dynamically updates the displayed collection metrics, student counts, and posted fees to match that selected unit (and shows all units when reset).

### Feature: Student Dashboard

US1: As a Student, I want to view my School-Wide Fees and Institutional/Department Fees on my dashboard so that I can track my Paid and Unpaid balances.
- AC1.1: The Student Dashboard displays the student's profile details (Name, ID, Year/Section) and separates fees into School-Wide Fees and Department/Institutional Fees tables with Amount, Date Paid, Time Paid, Status, and Receipt columns.

US2: As a Student, I want to check my real-time clearance status banner and read-only dashboard view so that I know whether I am cleared and cannot accidentally alter records.
- AC2.1: The clearance banner reflects real-time clearance status based on required fees, and the dashboard remains strictly read-only with no controls to edit fee amounts or change payment statuses.

US3: As a Student, I want to view the receipt for any fee marked as Paid so that I have proof of my completed payment.
- AC3.1: Fees marked Paid display a PAID badge, Date/Time Paid, and a clickable View button that opens the receipt, while Unpaid fees display an UNPAID badge with — for Date/Time Paid and no receipt button.
