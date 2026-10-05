# Lab 4 - Solved Lab Activities (Agile Estimation)

Scenario: the Lab 3 backlog, estimated once by the AI and once by the team in Planning Poker.

## Activity 1: Get AI estimates on the whole backlog
**Prompt:**
```
Estimate these user stories in story points on a Fibonacci scale (1,2,3,5,8,13). For each, give the number and one line on the main source of complexity. Assume a small team that is new to the codebase.
```
Example result: "register for an event" = 5 points, citing concurrency (two students racing for the last seat).

## Activity 2: Run Planning Poker and reveal
Everyone writes their estimate down first, then all reveal together. Team estimate for registration was 8 (AI said 5) because the event-capacity data model was not finalised, which the AI could not know.

## Activity 3: Line up every story
AI and team matched closely on simple stories (login, browse events) and diverged most where the team knew state was unsettled (registration, push notifications).

## Activity 4: Work out what fits in a sprint
Assume 20 points per two-week sprint. Six compared stories already total 31 team points, over one sprint's capacity. Bring that finding to sprint planning.

## My own run (fill in)
- Group members:
- Date/time of blind round:
- Tool used for AI estimates:
