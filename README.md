# Coachella Festival Analytics – Operational Efficiency and Revenue Insights

## 1. Project Background and Objective

The Coachella Valley Music and Arts Festival is a premier global event that draws over 250,000 attendees annually. As part of its commitment to providing exceptional experiences while maintaining operational efficiency, Coachella faces the recurring challenge of optimizing ticket sales, managing high-volume logistics, and ensuring balanced staff-to-stage coverage.

This project simulates a professional consulting engagement focused on extracting actionable insights from Coachella's operations database. The objective is to support strategic decision-making across departments—specifically revenue optimization, workforce allocation, and audience engagement.

*Key Focus Areas:*

* Ticket revenue segmentation and pricing strategy
* Stage-level staffing analysis and coverage assessment
* Genre-based artist performance evaluation
* Attendance patterns and peak congestion diagnostics

---

## 2. Data Architecture Overview

The relational database consists of multiple normalized tables reflecting real-world operations, enabling multidimensional analysis. Entities and relationships include:

* *Performance*: Details on artist appearances, scheduling, and stage assignments
* *Artist*: Genre classification, type of performance, and technical preferences
* *Stage*: Venue capacity and mapping to geographic zones
* *Ticket, Buyer, Order*: Commercial and demographic data
* *Employee*: Role, assignment, and shift-based labor data
* *Attends / Takes\_Place*: Participation and scheduling logs

📎 Full ERD and schema documentation are located in the /docs directory.

---

## 3. Executive Summary of Insights

*Key Findings:*

* VIP tickets account for 45% of total revenue despite lower unit sales, reflecting strong pricing power
* The East Zone is critically understaffed relative to its stage capacity, posing a significant operational risk
* April 12 emerged as the highest-traffic date, indicating potential scheduling bottlenecks
* Latin American and Pop artists demonstrate elevated attendance metrics, warranting deeper genre prioritization

These insights form the basis of targeted recommendations for Coachella's event planning and business strategy teams.

---

## 4. Analytical Findings by Business Domain

### A. Ticket Revenue Optimization

* VIP tickets generated disproportionately high revenue, validating premium pricing strategy
* Camping tickets exhibited low yield and underperformed relative to access privileges and stage proximity

➡ SQL query: GROUP BY Ticket_Type and aggregated revenue calculations

---

### B. Workforce Allocation Analysis

* East Zone manages high-capacity stages with minimal staff coverage—this imbalance compromises service quality and safety
* Recommendation: Redirect staffing from lower-utilization zones to support high-density performance areas

➡ SQL query: JOIN Stage, Employees via Area_ID; compute Capacity / Employee_Count

---

### C. Attendance and Scheduling Optimization

* April 12 accounted for the highest single-day attendance across all performances
* Suggest staggering marquee acts across different days to alleviate congestion and resource strain

➡ SQL query: Count distinct attendees grouped by performance date

---

### D. Artist Programming Strategy

* Pop and Latin genres dominate both artist count and audience engagement
* Latin acts consistently outperformed others in audience metrics, suggesting an opportunity to scale genre representation

➡ SQL query: GROUP BY Genre, Artist_Type for distribution and popularity trends

---

## 5. Strategic Recommendations

The following cross-functional recommendations are derived from the analyses:

1. *Increase employee assignment in East Zone* to ensure operational coverage and attendee experience
2. *Amplify VIP-tier marketing and bundling strategies* to maximize revenue from high-value segments
3. *Reassess camping ticket offerings*—consider either enhancement or repackaging due to low performance
4. *Distribute headline performances more evenly* across the festival calendar to balance peak loads
5. *Expand Latin genre programming*, leveraging demonstrated audience engagement and cultural resonance

---

## 6. Data Assumptions and Constraints

* Buyer and employee records were generated using Mockaroo and are representative only
* Ticket-to-performance mapping assumes one stage per ticket for simplification
* Duration of performances was derived from Start and End times without gaps or delays
* Workforce mobility across zones is not modeled—employees are treated as fixed to their assigned areas

---

## 7. Project Repository Structure



/coachella-festival-analytics

├── README.md        → Executive summary and final project deliverable  
├── /sql/            → Contains SQL database schema code and analytical queries (includes .sql and .docx files with detailed query explanations)  
├── /docs/           → Includes ERD diagrams, schema mapping, and key project assumptions  
├── /data/           → Cleaned and structured datasets (in CSV and Excel formats) used for analysis  
└── /visuals/        → Tableau dashboards and visual outputs with SQL-based insights (included as images)



---

## 8. Closing Statement

This project demonstrates a real-world analytics workflow that is stakeholder-facing and business-impact focused. It emphasizes data storytelling, operational KPIs, and SQL-driven insight generation tailored for a non-technical audience.

Thank you for reviewing this work. I welcome the opportunity to discuss my analytical thought process, data modeling approach, and how I can contribute to data-driven decision-making in your organization.
