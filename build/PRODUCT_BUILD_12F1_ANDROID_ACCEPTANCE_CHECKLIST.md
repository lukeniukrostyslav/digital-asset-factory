# BUILD-12F1 — Android Acceptance Checklist

Purpose: one physical Android acceptance pass; no repeated candidate builds.

## P0 — Navigation
- [ ] Root opens without error
- [ ] Home opens
- [ ] Today opens
- [ ] Capture opens
- [ ] Goals opens
- [ ] Projects opens
- [ ] Tasks opens
- [ ] Habits opens
- [ ] Reviews opens
- [ ] AI Assistant Hub opens
- [ ] Language Hub opens

## P1 — Mobile layout
- [ ] No required horizontal scrolling on primary pages
- [ ] Page titles readable
- [ ] Database rows/cards readable
- [ ] No important property clipped
- [ ] Buttons/links tappable without precision tapping
- [ ] Navigation remains usable after returning from a database page

## P2 — Core workflows
- [ ] Create one Life Area
- [ ] Create one Goal and link Life Area
- [ ] Create one Project and link Goal
- [ ] Create one Task and link Project
- [ ] Change Task status
- [ ] Set Task due date and priority
- [ ] Create one Capture
- [ ] Process Capture into its destination
- [ ] Open a Review

## P3 — Five-language smoke test
Repeat P0/P1 for EN, IT, FR, DE and RU. Check especially long labels and localized navigation.

## P4 — Acceptance evidence
A real Android screenshot/recording or equivalent device-level evidence is required for PASS. Notion connector structure inspection alone is not sufficient for visual PASS.

## Decision rule
PASS only if all P0/P1 critical items pass and no blocking mobile defect remains. Otherwise keep BUILD-12F below 100% and record the defect before release.

Current status: checklist prepared; physical device evidence not available through the current Notion connection, so no Android PASS is claimed.
