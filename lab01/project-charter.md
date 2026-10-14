# Project charter: Realtime Quiz platform

| Field    | Value                              |
|----------|------------------------------------|
| Version  | 1.0 (draft for sponsor approval)   |
| Date     | 2026-09-29                         |
| Sponsor  | Head of the IT department          |
| PM       | Kiv Sovannlyda, supervising lecturer    |

## 1. Purpose and justification
Lecturers currently spend too much time marking quizzes, and students lack instant feedback during sessions. This project will build the Realtime Quiz platform, allowing instructors to host live, timed sessions where students answer via a 6-character code, with scores updating instantly. This will eliminate manual marking and improve student engagement. See `business-case.md` for the financial justification.

## 2. Objectives and success criteria
| #  | Objective (what will be true)      | Success criterion (number + week) |
|----|------------------------------------|-----------------------------------|
| O1 | MVP built with all Must features   | 100% of Must features pass QA, week 7 |
| O2 | Pilot with 50 students in one live session | 50 participants, 0 blocking defects, week 14 |
| O3 | Broadcast latency during the pilot | <= 500 ms at the 95th percentile, measured week 14 |
| O4 | Server capacity handles concurrent load | 100 participants concurrently without crashing, tested week 13 |
| O5 | Code quality and test coverage met | >= 80% line coverage and green CI on merge, week 7 |

## 3. High-level scope
In scope:
- Multiple-choice quiz creator interface
- Real-time participation and updates over WebSocket
- Instant feedback and scoring system
- Live leaderboards
- Authentication and role management (Instructor, Student, Guest)

Out of scope:
- Native mobile applications (iOS/Android)
- Free-text or other non-multiple-choice question types
- Video conferencing integration
- LMS integration (Canvas, Moodle, etc.)

## 4. Milestones
| Week | Milestone                          | Ends process group |
|------|------------------------------------|--------------------|
| 1    | Charter approved, team formed      | Initiating         |
| 3    | PM plan and UI mockups approved    | Planning           |
| 7    | MVP demo                           | Executing          |
| 10   | Analytics and export features done | Executing          |
| 12   | Testing, hardening, and load test  | Monitoring and controlling |
| 13   | Operations runbook handed over     | Closing            |
| 14   | Pilot with 50 students, closure    | Closing            |

## 5. Budget summary
Effort:  students 4 x 14 x 8 h = 448 h; PM 14 x 3 h = 42 h; total 490 h
Cash:    hosting 4 x 25 USD = 100 USD; domain 15 USD; tools 60 USD; reserve 25 USD (14 %); total 200 USD

## 6. Assumptions
- The campus proxy network will not block WebSocket connections.
- The university will provide the 50 students required for the pilot.
- Lecturers will adopt the system if the pilot is successful.

## 7. Constraints
- The project must be completed within exactly 14 weeks.
- Total cash spending cannot exceed the 200 USD cap.
- The hosting is restricted to a Linode VPS at gicitc.com with 2 vCPU and 2 GB RAM.

## 8. High-level risks
- The campus proxy may block WebSocket (fallback: SockJS required).
- Client clocks may drift from the server, causing race conditions on late answers.
- The PDF export feature may fail to correctly render Khmer names.

## 9. Project manager authority
The PM decides alone on re-planning tasks, assigning student work, and spending within the 490 h and 200 USD base budget. The PM needs sponsor approval to add new scope, delay the week 14 pilot, or spend from the 25 USD cash reserve.

## 10. Approval
Sponsor: Head of the IT department  Date: 2026-10-14

PM:      Kiv Sovannlyda, supervising lecturer  Date: 2026-10-14