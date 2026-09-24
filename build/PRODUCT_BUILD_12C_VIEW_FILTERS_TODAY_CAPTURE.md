# PRODUCT-BUILD-12C — View Filters, Sorts, Today & Capture Layouts

## Status
Completed: 100% of the planned 12C implementation scope.

## Physical Notion work completed
Configured physical views with filters, sorting and mobile-focused visible properties:

- Tasks — Today: Status != Done; sorted by Due ascending; shows Task, Status, Due, Priority, Project.
- Tasks — This Week: Status != Done; sorted by Due ascending; shows Task, Status, Due, Priority, Project.
- Goals — Active: Status = Active; sorted by Progress descending.
- Projects — Active: Status = Active; sorted by Target Date ascending.
- Habits — Active: Status = Active.
- Reviews — Upcoming: Status != Completed; sorted by Period ascending.
- Captures — Inbox: Processed = FALSE; sorted by Created descending.
- Notes — Recent: sorted by Updated descending.

## Dedicated mobile-facing linked layouts
Created on physical Notion pages:

### Today
- Tasks — Today (Daily)
- view: view://3e529a2f-45ae-8158-83c0-000c5ef87eaf

### Capture
- Capture — Inbox (Process)
- view: view://3e529a2f-45ae-8118-92dd-000cef626f8f

## Important implementation note
The original Projects — Active view reference was no longer resolvable during this pass. Instead of claiming it was updated, a new physically configured replacement view was created:

- Projects — Active (Configured)
- view: view://3e529a2f-45ae-8149-b407-000c71052b77

## Quality boundary
12C is a physical configuration checkpoint, not Android visual acceptance. Mobile visual QA remains a separate gate.

## Next block
PRODUCT-BUILD-12D — Blank Workspace.
