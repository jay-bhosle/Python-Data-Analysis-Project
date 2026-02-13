✈️ Northern Lights Air Loyalty Campaign Analysis

Python | Pandas | EDA | Campaign Analytics | Behavioral Analysis

🖼️ Image 1 — Project Introduction

Business context and objectives defined:

Airline loyalty campaign (Feb–Apr 2018)

Measure campaign effectiveness

Analyze demographic adoption

Evaluate post-campaign engagement

<img width="1920" height="1080" alt="Screenshot (78)" src="https://github.com/user-attachments/assets/a008f5db-6562-407c-941b-4f04a65bc04e" />

🖼️ Image 2 — Library Imports
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt


Set up analysis environment.

<img width="1920" height="1080" alt="Screenshot (79)" src="https://github.com/user-attachments/assets/93f753f2-bea8-4987-90df-19615030051f" />

🖼️ Image 3 — Data Loading

Loaded:

Customer Loyalty History

Customer Flight Activity

Calendar

Data Dictionary

Validated .head() and .shape().

<img width="1920" height="1080" alt="Screenshot (80)" src="https://github.com/user-attachments/assets/f86ebb6d-94ac-411b-a088-e9e5e62f7855" />

🖼️ Image 4 — Dataset Shape & Overview

Confirmed:

16,737 loyalty members

392,936 flight records

Correct column structure

<img width="1920" height="1080" alt="Screenshot (81)" src="https://github.com/user-attachments/assets/4cedcbee-cab7-408f-98c4-66822c7bae47" />

🖼️ Image 5 — Loyalty Dataset Preview

Reviewed:

Demographics

Enrollment year/month

Cancellation year/month

Salary

CLV

<img width="1920" height="1080" alt="Screenshot (82)" src="https://github.com/user-attachments/assets/e0c88098-236c-4c5c-b49a-ce4dedd331b1" />

🖼️ Image 6 — Flight Activity Preview

Reviewed:

Year

Month

Total Flights

Distance

Points Accumulated

Points Redeemed

<img width="1920" height="1080" alt="Screenshot (83)" src="https://github.com/user-attachments/assets/dd2ab494-ef9e-472c-8be4-013759ec3608" />

🖼️ Image 7 — Data Dictionary Inspection

Validated column definitions and descriptions.

<img width="1920" height="1080" alt="Screenshot (84)" src="https://github.com/user-attachments/assets/f1901689-6005-472d-8ce3-a27255bb9b16" />


🖼️ Image 8 — Data Types Check (info())

Verified:

Correct datatypes

Null counts

Memory usage

<img width="1920" height="1080" alt="Screenshot (85)" src="https://github.com/user-attachments/assets/25ac62c8-5716-43c9-918a-cc17fdf9fd39" />

🖼️ Image 9 — Missing Values Analysis

Findings:

Salary missing (~4,238)

Cancellation fields missing (~14,670, expected)

No structural issues

<img width="1920" height="1080" alt="Screenshot (86)" src="https://github.com/user-attachments/assets/4f87674b-0a36-4e55-9373-595bae69ae1d" />

🖼️ Image 10 — Duplicate Check

Results:

Loyalty → 0 duplicates

Flight → acceptable monthly-level duplicates

<img width="1920" height="1080" alt="Screenshot (87)" src="https://github.com/user-attachments/assets/e1c40757-374f-4e57-8835-f73d78671b5e" />

🖼️ Image 11 — Column Cleaning

Standardized naming:

.lower()
.strip()
.replace(" ", "_")

<img width="1920" height="1080" alt="Screenshot (88)" src="https://github.com/user-attachments/assets/d8c301bd-a3ac-46ee-bb3e-2d896c710c44" />

🖼️ Image 12 — Enrollment Date Feature Engineering

Created:

enrollment_date


Converted year + month → datetime.

<img width="1920" height="1080" alt="Screenshot (89)" src="https://github.com/user-attachments/assets/a0157abc-e121-45f5-8f63-858ccadf6f54" />

🖼️ Image 13 — Campaign Period Classification

Defined campaign window:

Feb 2018 – Apr 2018


Created campaign_period:

pre_campaign

during_campaign

post_campaign

<img width="1920" height="1080" alt="Screenshot (90)" src="https://github.com/user-attachments/assets/d46ffd12-1577-4f50-9409-24e16f5db9a7" />

🖼️ Image 14 — Campaign Period Distribution

Customer counts:

Period	Members
Pre	13,919
During	971
Post	1,847

<img width="1920" height="1080" alt="Screenshot (91)" src="https://github.com/user-attachments/assets/9e25eb57-3a28-45af-b80d-1301d8e9a4a5" />

🖼️ Image 15 — Cancellation Date + Active Flag

Created:

cancellation_date

is_active

Validated date logic.

<img width="1920" height="1080" alt="Screenshot (92)" src="https://github.com/user-attachments/assets/4e864651-3172-4b41-8811-576e71fac902" />

🖼️ Image 16 — Monthly Enrollment Aggregation

Grouped monthly enrollments.

Calculated:

Gross enrollments

Cancellations

Net membership change

<img width="1920" height="1080" alt="Screenshot (93)" src="https://github.com/user-attachments/assets/0d485e79-3b80-40bd-a73f-de666c1192eb" />

🖼️ Image 17 — Campaign vs Non-Campaign Averages

Average monthly enrollments:

Period	Avg
During Campaign	323
Outside Campaign	202

🔥 ~60% increase during campaign.

<img width="1920" height="1080" alt="Screenshot (94)" src="https://github.com/user-attachments/assets/b98e2978-0351-463a-97f5-91e28dee9b7a" />

🖼️ Image 18 — Monthly Enrollment Trend (Line Chart)

Visualized:

Monthly enrollments

Campaign shaded region

Clear spike visible.

<img width="1920" height="1080" alt="Screenshot (95)" src="https://github.com/user-attachments/assets/525e867f-9aa1-49f9-979f-813d3ae974f4" />

🖼️ Image 19 — Cumulative Net Membership Growth

Plotted cumulative net members.

Strong upward trajectory.

<img width="1920" height="1080" alt="Screenshot (96)" src="https://github.com/user-attachments/assets/5f2bfc6c-b736-4abc-a520-3f486f2ee853" />

🖼️ Image 20 — Gender Adoption Analysis

Adoption rate by gender:

Minimal difference.

Campaign broadly neutral across genders.

<img width="1920" height="1080" alt="Screenshot (97)" src="https://github.com/user-attachments/assets/56d8b257-eb63-484d-baac-9439f7f13783" />

🖼️ Image 21 — Education Adoption Analysis

Adoption by education level:

Slightly higher for High School / Bachelor

Lower for Master / Doctor

<img width="1920" height="1080" alt="Screenshot (98)" src="https://github.com/user-attachments/assets/95fe98e8-d665-435a-ac96-2887820882ef" />

🖼️ Image 22 — Salary Band Creation

Segmented salary into:

<50K

50K–75K

75K–100K

100K+

Unknown

Prepared for adoption analysis.

<img width="1920" height="1080" alt="Screenshot (99)" src="https://github.com/user-attachments/assets/aa2ce42f-e724-4dbc-971f-7c7810972f06" />

🖼️ Image 23 — Salary Adoption Rate (Bar Chart)

Results:

Salary Band	Adoption Rate
<50K	16% 🔥
50K–75K	~5%
75K–100K	~4%
100K+	~4%
Unknown	~6%

🚀 Major Insight:
Lower-income segment most responsive.

<img width="1920" height="1080" alt="Screenshot (100)" src="https://github.com/user-attachments/assets/12f6233d-6f8a-4b32-b94d-3e1da6669ac4" />

🖼️ Image 24 — Summer Flight Filtering & Aggregation

Filtered:

May–August 2018

Grouped average flights by campaign_period.

<img width="1920" height="1080" alt="Screenshot (101)" src="https://github.com/user-attachments/assets/16a296f5-5315-4c53-ab49-153f069cbc1a" />

🖼️ Image 25 — Summer Flight Comparison (Bar Chart)

Results:

Campaign Group	Avg Flights
During Campaign	31
Pre Campaign	7
Post Campaign	2

🔥 Campaign joiners flew 4–12x more than others.

Strong behavioral activation.

🎯 Final Business Conclusions
1️⃣ Campaign Effectiveness

+60% enrollment growth

Significant net membership acceleration

2️⃣ Best Responding Segment

Customers earning <50K

3️⃣ High Engagement Lift

Campaign joiners flew significantly more

4️⃣ Strategic Direction

Focus on lower-income segment targeting

Retain high-activity customers

Predict churn using behavior signals

<img width="1920" height="1080" alt="Screenshot (102)" src="https://github.com/user-attachments/assets/ed26364b-9d32-4e26-83c5-77489f64d423" />

🛠 Tech Stack

Python

Pandas

NumPy

Matplotlib

Jupyter Notebook
