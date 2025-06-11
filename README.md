# Call-Center-Operational-Efficiency-Dashboard

## Overview

This project presents a Power BI dashboard designed to analyze and visualize key metrics related to a customer service call center, including agent performance, IVR interactions, and escalation trends. The data is sourced from a MySQL database and analyzed through Power BI, running on an AWS EC2 instance for performance efficiency.

---

## Table of Contents

- [Home](![Home page](https://github.com/user-attachments/assets/6a39e131-4e0d-4bd8-9e1a-69b63bf834f8)
)
- [Agent Performance](#agent-performance)
- [IVR Interaction Behavior](#ivr-interaction-behavior)
- [Escalation](#escalation)
- [Findings](#findings)
- [Infrastructure](#infrastructure)

---

## Home

The **Home** page serves as the entry point of the dashboard. It includes:

- A small logo and clean layout.
- Visuals:
  - **Donut chart**: Call status (e.g., Resolved, Dropped, Escalated).
  - **Bar chart**: Total calls by agent.
  - **Line chart**: Total calls over months.
  - **KPI cards**:
    - Total calls
    - Average call duration
    - Drop rate %
    - Escalation rate %
    - Resolved rate %
- Interactive elements:
  - Slicers: Team, Date Range, Call Status.
  - Navigation buttons for easy access to all pages.

---

## Agent Performance

This page is focused on evaluating **individual agent performance**. It includes:

- **Line charts**: 
  - Average call duration by agent.
  - Escalation rate by agent.
- **Bar chart**: Total calls handled by agent.
- **Custom table**: Summarized data with key metrics.
- **Column chart**: Call status categorized by Agent ID.
- **KPI card**: Number of active agents.
- **Slicers**: Shift Timing, Teams, Call Status.

---

## IVR Interaction Behavior

The **IVR Interaction** page provides insights into how customers interact with the IVR system:

- **Line chart**: Dropped call % by day — helps identify IVR efficiency.
- **Pie chart**: Call disposition count by category.
- **Column chart**: Call duration by IVR path — identifies commonly asked queries.
- **Slicers**: Team, Date Range, Call Status.

This page helps in understanding:
- Whether calls were resolved without human interaction.
- How efficient and intuitive the IVR path is.
- Need for additional IVR options or improvements.

---

## Escalation

The **Escalation** page analyzes the cases that were not resolved initially and had to be escalated:

- **Bar chart**: Escalated vs Total calls by team.
- **Table**: Filterable by agent for deeper insights.
- **Slicers**: Same as previous pages (Team, Date, Status).

Key observations:
- Escalated call rate ~20% — not critical, but improvement is needed.
- Escalation data can be used to add options to IVR or improve agent training.
- Drop rate (23%) is high — worth investigating further.

---

## Findings

- **Call Drop Rate**: Around 23–24% — potentially due to IVR resolution or technical issues. Needs to be reduced to below 10%.
- **Resolved Call Rate**: Too low — should be consistently above 50%.
- **Escalation Rate**: Acceptable at 20%, but improvements could still be made.
- **Monthly Trend**: June showed fewer calls than May — could indicate a need for improved sales efforts.
- **Call Volume by Agent**: Evenly distributed, since the IVR connects calls automatically.
- **Customer Patterns**: Call paths and durations indicate frequently asked questions — good for building self-help resources.

---

## Infrastructure

- **Environment**: AWS EC2 instance (Windows OS via RDP) used for running Power BI.
- **Reason**: High computing power requirement — local laptop is insufficient.
- **AWS Services Used**:
  - **EC2**: Hosting Power BI.
  - **Redshift, Glue, Athena, Lambda**: Target services for expansion.
- **Database**: MySQL
  - Connected via ODBC.
  - Initial SQL queries helped understand data structure.
  - Two tables linked via primary key.
- **Data**: Recent 1,000 IVR call records.

---

## Conclusion

This Power BI project helps stakeholders understand performance at multiple levels — from individual agents to system-wide IVR efficiency. With clear visuals and interactivity, it allows data-driven decisions for improving customer service operations.

---

## Author

**[Your Name]**  
_Data Analyst | AWS Enthusiast | Power BI Developer_

---

