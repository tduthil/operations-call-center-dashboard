📊 Call Center Performance Analytics Dashboard

Tools: Power BI | Python | DAX
Dataset: 61,545 call interactions across 3 teams (30 agents) over 3 months
Role: Business Analyst | Data Visualization Developer

Business Challenge
Operations leadership needed real-time visibility into call center performance across multiple dimensions: team, agent, and time of day, to identify coaching opportunities, optimize scheduling, and improve customer satisfaction. The existing Excel-based reporting system required manual updates and lacked interactive drill-down capabilities.

Business Insights & Impact
Operational Findings:

Peak Hour Identification: 
* Call volume peaks at 9 AM, 11 AM, and 2 PM (9.4K, 9.3K, 9.1K calls respectively) enabled optimized break scheduling
* Call Type Analysis: Escalated and Callback Scheduled calls show 15-20% higher AHT, indicating complexity drivers
* Performance Distribution: 47% of interactions are exceeding AHT expectations, 34% need targeted coaching
* CSAT Correlation: Preliminary analysis shows inverse relationship between AHT and CSAT (requires further statistical validation)

Example Impact (based on industry benchmarks):

* Reduced manual reporting time from 4 hours/week to 15 minutes
  
* Division Leader can view team performance and identify underperforming teams at glance
<img width="1122" height="771" alt="image" src="https://github.com/user-attachments/assets/fe807453-2557-4ef3-8dc2-c7eecc046f50" />

Team Leader can view agent performance and identify call types and agents needing coaches
<img width="1112" height="761" alt="image" src="https://github.com/user-attachments/assets/2facc527-03ac-4960-bafe-30c716793b76" />

Agents can view individual performance and call types that need to be optimized
<img width="1091" height="763" alt="image" src="https://github.com/user-attachments/assets/3b2da775-9850-430e-af98-5107d1ad569d" />

Solution
Designed and developed a three tier interactive dashboard in Power BI providing executive, teaam, and agent-level insights into call center operations.

Dashboard Architecture:

Executive/Division Leader Overview Dashboard

* High-level KPIs: 61.5K interactions, 293.94 avg AHT, 74.42 CSAT, 63% FCR
*bHourly volume patterns identifying peak hours (9-11 AM, 2-4 PM)
* Call outcome distribution showing 27% resolution rate
* Performance segmentation: 47% meeting expectations, 34% exceeding


Team Leader Performance Dashboard

* Team-level comparisons across all metrics
* Interactive filtering by team, agent, and time period
8 AHT trends by hour showing team-specific patterns
* Top 10 longest calls for exception management


Agent Performance Dashboard

* Individual agent metrics with drill-down detail
* Call outcome distribution by agent
* AHT by call type & performance tracking for coaching conversations


Technical Implementation
Data Engineering:

* Generated synthetic dataset using Python (pandas, numpy) simulating realistic call center patterns
* Implemented business rules: volume spikes on Mondays/month-end, call type complexity variations, agent performance distributions
* Created data model with appropriate relationships and calculated columns

Visualization Choices:

* Donut charts for categorical breakdowns (call outcomes, performance distribution)
* Line charts for temporal trends (AHT by hour)
* Bar charts for comparisons (volume by hour, AHT by call outcome)
* KPI cards with conditional formatting for at-a-glance status

