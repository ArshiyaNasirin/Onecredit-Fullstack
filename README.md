# Onecredit Fullstack - Project Concept for Evaluation

This branch is intentionally documentation-only and contains a single file: `README.md`.

## 1. Executive Summary

Onecredit Fullstack (implemented here as a FieldDesk Advisor Hub experience) is an advisor-first agricultural decision platform.

Core idea:
- Most agritech products target farmers directly.
- Adoption is often low because farmers trust local advisors more than unfamiliar apps.
- This project equips the advisor (FPO officer/agronomist) with a high-leverage tool so one trained advisor can improve outcomes for hundreds of farmers.

In one line:
Advisor tool first, farmer impact at scale.

## 2. Problem Statement

Current field reality in many regions:
- One advisor handles 500 to 900 farmers.
- Prioritization is mostly manual, memory-based, and reactive.
- Soil recommendations are often generic and not cost-optimized.
- Follow-up communication lacks structure and measurable feedback.

Resulting pain points:
- Critical farmers may be missed.
- Input cost waste increases.
- Recommendation adoption is inconsistent.
- Institutions cannot prove advisor impact clearly.

## 3. Why This Concept Matters

The project reframes the problem from "farmer app adoption" to "advisor decision quality and throughput."

Conceptual shift:
- Old model: App -> Farmer (high behavior change burden)
- Proposed model: Platform -> Advisor -> Farmers (trust channel already exists)

Evaluation value:
- Lower adoption friction
- Faster deployment through existing institutions
- Measurable operational metrics from day 1

## 4. Target Users and Beneficiaries

Primary users:
- FPO officers
- Extension agronomists
- Field advisors

Secondary beneficiaries:
- Farmers receiving clearer, contextual recommendations
- Institutions (FPOs, agri programs) needing traceable outcomes

## 5. Product Concept and Theory of Change

### Inputs
- Farmer portfolio data
- Soil test values
- Weather forecasts
- Advisor field notes

### Process
1. Identify priority farmers
2. Generate crop-specific, cost-aware recommendations
3. Deliver advisor-branded, actionable message
4. Track confirmation and portfolio outcomes

### Outputs
- Faster response to high-risk cases
- Better fertilizer decisions
- Structured follow-up actions

### Outcomes
- Reduced avoidable input spend
- Higher recommendation follow-through
- Improved expected yield bands

## 6. End-to-End User Journey (Evaluation Narrative)

1. Advisor enters the app and sees an operations command center.
2. Priority queue highlights urgent farmers first.
3. Advisor opens Farmer 360 view for context: profile, history, current risk.
4. Soil values are entered or reviewed.
5. System generates a recommendation with estimated savings and yield range.
6. Advisor sends guidance through WhatsApp-style output.
7. Advisor tracks whether action was confirmed.
8. Institution reviews village and portfolio-level impact in insights dashboard.

This journey is the core evaluation story from intervention to measurable effect.

## 7. What Is Innovative Here

- Advisor-centric workflow rather than farmer-only app design
- Priority-first UI that matches field constraints
- Soil recommendation flow tied to cost and actionability
- Communication layer grounded in trusted advisor channel
- Built-in pilot evidence generation for institutional decisions

## 8. Modules and Pages (Concept + Function)

### Intro and Story (`/`)
Concept role:
- Explain mission, team, and real-world scenarios quickly.

### Command Center (`/portfolio`)
Concept role:
- Daily mission control for advisor workload and urgency management.

### Portfolio Live (`/portfolio-live`)
Concept role:
- Operational list management for real-time filtering and updates.

### Farmer 360 (`/farmer/:id`)
Concept role:
- Unified decision context for one farmer before advisor action.

### Soil Intelligence (`/farmer/:id/soil`)
Concept role:
- Translate lab inputs into practical recommendation outputs.

### Advisor Intelligence (`/insights`)
Concept role:
- Convert individual actions into portfolio-level evidence.

## 9. Evaluation Framework (How to Judge Success)

### Operational KPIs
- Time to identify top-priority farmers
- Number of high-risk farmers handled per day
- Recommendation turnaround time

### Adoption KPIs
- Recommendation sent rate
- Confirmation rate after message delivery
- Repeat usage by advisors

### Agronomic and Economic KPIs
- Estimated input cost reduction per acre
- Share of recommendations with expected yield improvement
- Seasonal trend in risk status mix (red/yellow/green)

### Institutional KPIs
- Exportable reporting readiness
- Village-level intervention visibility
- Decision support usefulness for supervisors

## 10. Pilot Design Suggestion

Recommended pilot shape:
- Duration: 8 weeks
- Geography: 1 district, 2 to 3 advisor teams
- Baseline period: first 1 to 2 weeks
- Intervention period: remaining weeks

Suggested measurable checkpoints:
- Week 2: prioritization accuracy and workflow usability
- Week 4: recommendation delivery consistency
- Week 6: farmer action confirmation trends
- Week 8: cost/yield proxy impact and institutional feedback

## 11. Assumptions, Risks, and Mitigation

Assumptions:
- Advisors remain the trusted communication layer.
- Soil data quality is reasonably usable.
- Institutions value outcome dashboards.

Risks:
- Backend downtime can limit live mode usage.
- Data inconsistency can reduce analytics quality.
- Workflow burden may increase if UI is not streamlined.

Mitigation:
- Demo mode ensures continuity for showcase and training.
- Structured data validation and normalized village naming.
- Clear quick actions and simplified advisor flow design.

## 12. Ethical and Practical Considerations

- Recommendations support advisors, not replace domain judgment.
- Transparency in confidence and uncertainty is essential.
- Data should be handled with institutional privacy safeguards.

## 13. Scalability View

Near-term scale path:
- More villages -> more advisors -> larger portfolio coverage
- Standardized dashboards for regional programs
- Integration with institutional procurement and reporting workflows

## 14. Team

- Naveen Raj B
- Arshiya Nasirin M
- Kabilan M
- Meganathan R
- Latchana S

## 15. Technical Appendix (Concise)

Routes:
- `/`
- `/portfolio`
- `/portfolio-live`
- `/insights`
- `/farmer/:id`
- `/farmer/:id/soil`

Data modes:
- Demo mode for full workflow without backend
- Live mode through API base URL (`VITE_API_URL`)

Stack:
- React + TypeScript + Vite
- Tailwind + component primitives
- Framer Motion
- Recharts
- Axios + React Query

## 16. Branch Note

This branch was created specifically for evaluation documentation.
Only this README file is intentionally included.