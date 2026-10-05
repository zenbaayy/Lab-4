# Lab 4 - Graded Lab Tasks (10 marks)

## Task 1 (3 marks): Estimate blind, then reveal
> Replace Member A/B/C with your group's real written estimates. Add timestamps or a witness.

| Story | Member A | Member B | Member C | Agreed |
|-------|----------|----------|----------|--------|
| US-01 Login | 3 | 5 | 3 | 3 |
| US-02 Browse events | 2 | 3 | 2 | 3 |
| US-03 Register | 8 | 5 | 8 | 8 |
| US-04 Cancel registration | 3 | 3 | 5 | 3 |
| US-05 Reminder | 8 | 13 | 8 | 8 |
| US-06 Admin add event | 5 | 3 | 5 | 5 |
| US-07 Admin remove event | 2 | 3 | 3 | 3 |
| US-08 View my registrations | 3 | 2 | 3 | 3 |
| US-11 Admin edit event | 5 | 5 | 3 | 5 |
| US-12 Notify on cancellation | 8 | 8 | 13 | 8 |

Biggest disagreements: US-05 and US-12 (8 to 13). Low estimators assumed an existing reminder set-up; the high estimator counted the scheduler and delivery work still to be built.

## Task 2 (3 marks): AI as a fourth voice, with assumption audit
| Story | Team | AI | Diff | AI justification | Audit verdict |
|-------|------|----|------|------------------|---------------|
| US-01 | 3 | 3 | 0 | "Standard auth flow" | Assumed (auth method not in backlog) |
| US-02 | 3 | 2 | +1 | "Read-only list" | Knowable |
| US-03 | 8 | 5 | +3 | "Concurrency on last seat" | Assumed (no seat limit in story) |
| US-04 | 3 | 3 | 0 | "Reverse of register" | Knowable |
| US-05 | 8 | 5 | +3 | "Scheduled email job" | Assumed (channel not specified) |
| US-06 | 5 | 3 | +2 | "Simple CRUD form" | Assumed (assumes admin UI exists) |
| US-07 | 3 | 2 | +1 | "Delete a record" | Assumed (ignores registrations) |
| US-08 | 3 | 2 | +1 | "Query and list" | Knowable |
| US-11 | 5 | 3 | +2 | "Reuse the add form" | Assumed |
| US-12 | 8 | 3 | +5 | "Trigger existing notification" | Assumed (reminders not built yet) |

**Audit count:** 3 Knowable, 7 Assumed. Totals: team 49 points, AI 31 points.

## Task 3 (2 marks): Three biggest gaps with team knowledge
1. **US-12 (gap 5):** the AI cannot know our reminder module is only designed, with no cancellation hook and no decision on email vs phone contact. Building that delivery path is most of this story.
2. **US-03 (gap 3):** the AI cannot know our event-capacity schema is not finalised, and that none of us has handled two students racing for the last seat in our chosen database.
3. **US-05 (gap 3):** the AI cannot know we have not picked a job scheduler or email provider, and that our university mail domain may rate-limit bulk mail.

## Task 4 (2 marks): Sprint capacity and confidence
- Sprint: 2 weeks (10 working days), 3 members.
- Velocity: 3 members x 10 days x about 3 focused hours = 90 hours. At about 4 hours per point for a team new to the codebase, 90 / 4 = 22.5 points. Rounded down to **20** as a buffer.
- Sprint 1: US-01 (3) + US-02 (3) + US-06 (5) + US-03 (8) = **19 points**, under 20.
- Later sprints: US-04 (3) + US-05 (8) + US-07 (3) + US-08 (3) + US-11 (5) + US-12 (8) = 30 points. Total 49 points, about 2.5 sprints, planned as 3.
- Confidence: I expect to be wrong by about 30 percent (real velocity 14 to 26 points). At the end of the sprint I will measure points actually completed against the 19 committed, plus real hours spent on US-03.

## Take-home
Re-estimate the same backlog a week later without looking at your earlier numbers. Report drift per story, and say whether drift was larger where you disagreed with the AI or agreed with it.
