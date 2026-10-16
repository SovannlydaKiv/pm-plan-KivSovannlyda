# Post-mortem: CampusPay wallet (fictional case)

## 1. Timeline and sources
| # | When | Event | Source |
|---|------|-------|--------|
| 1 | Month 1 | University IT asked to build cashless app for canteen and library | fictional case from Lab-01 |
| 2 | Month 1 | Head of finance "sponsors" via email but does not formally sign a charter | fictional case from Lab-01 |
| 3 | Month 2 | Developer acts as PM and sets sole goal as "launch in September" | fictional case from Lab-01 |
| 4 | Month 3 | Requirements expand to bus tickets and parking based on a survey | fictional case from Lab-01 |
| 5 | Month 4 | Development finishes; no testing is done with real card terminals | fictional case from Lab-01 |
| 6 | Day 1 Launch | Terminals reject 40% of payments; canteen queues double | fictional case from Lab-01 |
| 7 | Day 3 | App is entirely withdrawn due to failures | fictional case from Lab-01 |
| 8 | Month 9 | App relaunches five months later, restricted to canteen only | fictional case from Lab-01 |

## 2. Classification and organisation
Project / programme: This was a project (temporary and unique). 
Structure and PM authority: The structure was likely a weak matrix or purely functional, as a lead developer acted as both PM and coder with very little authority to control scope. 
Sponsor, charter, PMO: There was an "email sponsor" who was disengaged (never attended reviews), no formal project charter to authorize work, and no evidence of a PMO to enforce standards.

## 3. Success criteria
Stated: "Launch in September". 
Missing measurable criteria: Acceptable transaction failure rate (e.g., < 1%), maximum transaction time (e.g., < 2 seconds), and hardware compatibility requirements.
Ignored dimensions: Users (students and canteen staff suffered doubled queues) and Operations (real-world hardware integration with the existing card terminals was ignored).

## 4. Process groups and knowledge areas
| Process group              | What went wrong or was skipped |
|----------------------------|--------------------------------|
| Initiating                 | No formal charter; the head of finance never accepted the sponsor role, so nobody could refuse the bus-ticket scope creep. |
| Planning                   | Requirements were gathered via survey without technical feasibility planning or risk planning for the hardware integration. |
| Executing                  | The lead developer built features outside the original scope (parking, buses) instead of focusing on core functionality. |
| Monitoring and controlling | Progress was reported as "on schedule" without a single end-to-end test on real hardware, falling into the invisibility trap. |
| Closing                    | The product crashed into operations and was withdrawn rather than having a planned handover and pilot phase. |

Knowledge areas most responsible: Project Scope Management (uncontrolled feature creep), Project Quality Management (failure to test on real terminals), and Project Stakeholder Management (disengaged sponsor and ignored end-user impact).

## 5. Ethics
Decision examined: The decision to launch the app without testing it on real card terminals. 
Responsibility / respect / fairness / honesty: This decision violated **responsibility** (failing to ensure the product met basic operational requirements before release), **respect/fairness** (ignoring the severe negative impact on canteen staff and hungry students), and **honesty** (implicitly claiming the system was ready for launch when it had never been properly verified).

## 6. What our project will do differently
| # | Commitment (We will ...) | Measured by | By week | Charter line |
|---|--------------------------|-------------|---------|--------------|
| 1 | We will run a live session with 100 simulated students and the real campus proxy before the pilot | load test report, 0 errors | 12 | milestone week 12, O4 capacity |
| 2 | We will hold a signed charter with a named sponsor who attends the week-7 and week-13 gates | signature on charter, gate minutes | 1 | section 10 approval, authority clause |
| 3 | We will strictly control scope to multiple-choice questions for the MVP and reject other types | scope document, 0 non-MCQ features | 7 | section 3 High-level scope, out of scope |
| 4 | We will define success with specific quality metrics rather than just a launch date | measured latency <= 500ms | 14 | O3 latency |
| 5 | We will transition to operations smoothly with a defined runbook and checklist | operations handover sign-off | 13 | milestone week 13, section 3 handover |