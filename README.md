✈️ Northern Lights Air Loyalty Campaign Analysis

Python | Pandas | EDA | Campaign Impact | Behavioral Analytics

🖼️ Page 1 — Business Context & Objective

Northern Lights Air (NLA) launched a loyalty enrollment campaign (Feb–Apr 2018).

🎯 Objectives:

Measure campaign impact on enrollments

Evaluate demographic adoption

Analyze post-campaign engagement

Generate strategic recommendations

<img width="1920" height="1080" alt="Screenshot (78)" src="https://github.com/user-attachments/assets/a008f5db-6562-407c-941b-4f04a65bc04e" />

🖼️ Page 2 — Environment Setup
import pandas as pd
import numpy as np


Configured display settings and initialized analysis environment.

<img width="1920" height="1080" alt="Screenshot (79)" src="https://github.com/user-attachments/assets/93f753f2-bea8-4987-90df-19615030051f" />

🖼️ Page 3 — Data Loading

Loaded datasets:

Customer Loyalty History

Customer Flight Activity

Calendar

Data Dictionary

Validated row counts and structure.

<img width="1920" height="1080" alt="Screenshot (80)" src="https://github.com/user-attachments/assets/f86ebb6d-94ac-411b-a088-e9e5e62f7855" />

🖼️ Page 4 — Dataset Shapes & Preview

Confirmed dataset sizes:

Dataset	Rows	Columns
Loyalty	16,737	16
Flight	392,936	8

Displayed .head() for validation.

<img width="1920" height="1080" alt="Screenshot (81)" src="https://github.com/user-attachments/assets/4cedcbee-cab7-408f-98c4-66822c7bae47" />

🖼️ Page 5 — Flight Activity Inspection

Reviewed:

Year / Month

Total Flights

Distance

Points Accumulated

Points Redeemed

Confirmed monthly-level granularity.

<img width="1920" height="1080" alt="Screenshot (82)" src="https://github.com/user-attachments/assets/e0c88098-236c-4c5c-b49a-ce4dedd331b1" />

🖼️ Page 6 — Data Dictionary Review

Verified column definitions and business meanings.

Ensured correct interpretation of metrics.

<img width="1920" height="1080" alt="Screenshot (83)" src="https://github.com/user-attachments/assets/dd2ab494-ef9e-472c-8be4-013759ec3608" />

🖼️ Page 7 — Data Types & Structure

Used:

.info()


Validated:

Correct datatypes

Memory footprint

Null presence

<img width="1920" height="1080" alt="Screenshot (84)" src="https://github.com/user-attachments/assets/f1901689-6005-472d-8ce3-a27255bb9b16" />


🖼️ Page 8 — Missing Values Analysis

Key findings:

Cancellation fields mostly null → expected

Salary missing (~4,238)

No critical data corruption

<img width="1920" height="1080" alt="Screenshot (85)" src="https://github.com/user-attachments/assets/25ac62c8-5716-43c9-918a-cc17fdf9fd39" />

🖼️ Page 9 — Duplicate Check

Loyalty: 0 duplicates

Flight activity: acceptable monthly-level repetition

Data integrity confirmed.

<img width="1920" height="1080" alt="Screenshot (86)" src="https://github.com/user-attachments/assets/4f87674b-0a36-4e55-9373-595bae69ae1d" />

🖼️ Page 10 — Column Standardization

Cleaned column names:

Lowercase

Replaced spaces with underscores

Removed inconsistencies

Prepared for transformation.

<img width="1920" height="1080" alt="Screenshot (87)" src="https://github.com/user-attachments/assets/e1c40757-374f-4e57-8835-f73d78671b5e" />

🖼️ Page 11 — Enrollment Date Engineering

Created:

enrollment_date


Combined:

enrollment_year + enrollment_month


Converted to datetime format.

<img width="1920" height="1080" alt="Screenshot (88)" src="https://github.com/user-attachments/assets/d8c301bd-a3ac-46ee-bb3e-2d896c710c44" />

🖼️ Page 12 — Campaign Period Classification

Defined campaign window:

Feb 2018 – Apr 2018


Created:

campaign_period


Distribution:

Period	Members
Pre	13,919
During	971
Post	1,847

<img width="1920" height="1080" alt="Screenshot (89)" src="https://github.com/user-attachments/assets/a0157abc-e121-45f5-8f63-858ccadf6f54" />

🖼️ Page 13 — Cancellation Date & Active Flag

Created:

cancellation_date

is_active

Validated no illogical timelines.

<img width="1920" height="1080" alt="Screenshot (90)" src="https://github.com/user-attachments/assets/d46ffd12-1577-4f50-9409-24e16f5db9a7" />

🖼️ Page 14 — Monthly Enrollment Aggregation

Grouped by Year-Month.

Calculated:

Gross enrollments

Cancellations

Net membership change

Prepared time-series view.

<img width="1920" height="1080" alt="Screenshot (91)" src="https://github.com/user-attachments/assets/9e25eb57-3a28-45af-b80d-1301d8e9a4a5" />

🖼️ Page 15 — Campaign vs Non-Campaign Comparison

Average monthly enrollments:

Period	Avg Enrollments
During Campaign	~323
Outside Campaign	~202

🔥 ~60% enrollment lift.

<img width="1920" height="1080" alt="Screenshot (92)" src="https://github.com/user-attachments/assets/4e864651-3172-4b41-8811-576e71fac902" />

🖼️ Page 16 — Monthly Enrollment Trend Visualization

Line chart:

Monthly enrollments

Campaign period shaded

Clear spike during campaign months.

<img width="1920" height="1080" alt="Screenshot (93)" src="https://github.com/user-attachments/assets/0d485e79-3b80-40bd-a73f-de666c1192eb" />

🖼️ Page 17 — Cumulative Net Membership Growth

Plotted cumulative net members.

Result:
Strong upward trajectory post-campaign.

<img width="1920" height="1080" alt="Screenshot (94)" src="https://github.com/user-attachments/assets/b98e2978-0351-463a-97f5-91e28dee9b7a" />

🖼️ Page 18 — Gender Adoption Analysis

Campaign enrollments:

Gender	Count
Female	494
Male	477

Minimal difference in adoption rate.
<img width="1920" height="1080" alt="Screenshot (95)" src="https://github.com/user-attachments/assets/525e867f-9aa1-49f9-979f-813d3ae974f4" />

🖼️ Page 19 — Education Adoption Analysis

Adoption higher among:

High School

Bachelor

Lower among:

Master

Doctor

Moderate skew toward mid-education tiers.

<img width="1920" height="1080" alt="Screenshot (96)" src="https://github.com/user-attachments/assets/5f2bfc6c-b736-4abc-a520-3f486f2ee853" />

🖼️ Page 20 — Salary Band Creation

Created bands:

<50K

50K–75K

75K–100K

100K+

Unknown

Handled missing salary values.

<img width="1920" height="1080" alt="Screenshot (97)" src="https://github.com/user-attachments/assets/56d8b257-eb63-484d-baac-9439f7f13783" />

🖼️ Page 21 — Salary Adoption Rate Visualization

Adoption rates:

Salary Band	Rate
<50K	~16% 🔥
50K–75K	~5%
75K–100K	~4%
100K+	~4%
Unknown	~6%

📌 Strongest response from lower-income segment.

<img width="1920" height="1080" alt="Screenshot (98)" src="https://github.com/user-attachments/assets/95fe98e8-d665-435a-ac96-2887820882ef" />

🖼️ Page 22 — Summer Flight Filtering

Filtered:

Year = 2018

Months = May–August

Prepared engagement analysis.

<img width="1920" height="1080" alt="Screenshot (99)" src="https://github.com/user-attachments/assets/aa2ce42f-e724-4dbc-971f-7c7810972f06" />

🖼️ Page 23 — Summer Flight Aggregation

Grouped average flights by campaign_period.

Calculated engagement lift.

<img width="1920" height="1080" alt="Screenshot (100)" src="https://github.com/user-attachments/assets/12f6233d-6f8a-4b32-b94d-3e1da6669ac4" />

🖼️ Page 24 — Summer Flight Comparison Visualization

Results:

Campaign Group	Avg Flights
During Campaign	31.17
Pre Campaign	6.97
Post Campaign	2.46

🔥 Campaign joiners flew 4–12x more.

<img width="1920" height="1080" alt="Screenshot (101)" src="https://github.com/user-attachments/assets/16a296f5-5315-4c53-ab49-153f069cbc1a" />

🖼️ Page 25 — Final Recommendations
Strategic Recommendations:

Retain high-value campaign joiners

Target lower-income segments in future campaigns

Personalize incentives by loyalty tier

Monitor declining flight activity to predict churn

Focus retention on high-CLV customers

<img width="1920" height="1080" alt="Screenshot (102)" src="https://github.com/user-attachments/assets/ed26364b-9d32-4e26-83c5-77489f64d423" />

📊 Key Takeaways

✔ Campaign drove significant enrollment lift
✔ Lower-income segment most responsive
✔ Campaign joiners show strong behavioral engagement
✔ Post-campaign retention strategy critical
