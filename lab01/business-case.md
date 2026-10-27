# Business case: live quizzes for the IT department

## 1. Problem
Lecturers in the IT department spend an excessive amount of manual effort grading paper-based or basic digital quizzes, taking time away from actual teaching and course preparation. 
Assumptions:
- lecturers running quizzes: 10
- marking time per lecturer per week: 1 h
- teaching weeks per year: 30
- notional value of one hour: 10 USD (students are unpaid; used to compare)

## 2. Options
| Option | Description | One-off cost | Annual cost | Annual benefit |
|--------|-------------|--------------|-------------|----------------|
| A      | Do nothing  | 0            | 0           | 0              |
| B      | Buy SaaS    | 0            | 1,800       | 3,000          |
| C      | Build       | 4,900        | 300         | 4,800          |

*(Note: Option B assumes an educational SaaS like Kahoot! Pro priced at an assumed 15 USD per lecturer per month).*

## 3. Comparison
| Option | Net annual benefit | Payback (years) | Sensitivity (6 lecturers) |
|--------|--------------------|-----------------|----------------------------|
| B      | 3,000 - 1,800 = 1,200 | 0 (no one-off) | 1,800 - 1,080 = 720   |
| C      | 3,000 + 1,800 - 300 = 4,500 | 4,900 / 4,500 = 1.1 | 2,880: 1.7 |

## 4. Benefits not priced
- **Learning outcome:** The 4 software engineering students gain critical, hands-on capstone project experience.
- **Data ownership:** The university retains full control over student names, data, and privacy.
- **No per-seat limit:** The IT department can expand usage to more lecturers in the future without paying extra monthly SaaS license fees per seat.

## 5. Risks per option
**Option B (Buy SaaS):**
- The SaaS provider raises their educational pricing next year, impacting the department's tight budget.
- The platform stores student data offshore, violating the Data Protection Officer's retention and privacy policies.

**Option C (Build):**
- Client clocks drift from the server, causing race conditions and inaccurate scoring.
- The campus proxy blocks WebSocket traffic, degrading the real-time experience.

## 6. Recommendation and review gate
Recommendation: Option C (Build). The project pays for itself in just over one academic year (1.1 years) even with only 10 lecturers. Additionally, the department keeps its data on-premises and provides the capstone students with a valuable learning outcome. 

Review gate: If the MVP demo in week 7 fails to deliver the Must features, the sponsor will buy Option B (SaaS) for the next semester and treat the build as a two-semester project.