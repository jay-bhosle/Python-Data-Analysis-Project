<img width="1920" height="1080" alt="Screenshot (95)" src="https://github.com/user-attachments/assets/4512014e-3835-4ccb-838d-d4dcef9c3a78" /><img width="1920" height="1080" alt="Screenshot (80)" src="https://github.com/user-attachments/assets/832799f5-58d2-4b99-a742-c72372c2dfce" /><img width="1920" height="1080" alt="Screenshot (79)" src="https://github.com/user-attachments/assets/8d365c6e-ebad-466a-8e59-a259858f9bf0" />✈️ Northern Lights Air Loyalty Campaign Analysis

Python | Pandas | EDA | Campaign Analytics | Behavioral Analysis

🖼️ Image 1 — Project Introduction

Business context and objectives defined:

Airline loyalty campaign (Feb–Apr 2018)

Measure campaign effectiveness

Analyze demographic adoption

Evaluate post-campaign engagement
<img width="1920" height="1080" alt="Screenshot (78)" src="https://github.com/user-attachments/assets/ff9d3f78-35c7-46f7-bc0f-39060f00a65d" />

🖼️ Image 2 — Library Imports
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt


Set up analysis environment.
<img width="1920" height="1080" alt="Screenshot (79)" src="https://github.com/user-attachments/assets/44ece970-0594-4f8b-8813-d4ae6fdae975" />

🖼️ Image 3 — Data Loading

Loaded:

Customer Loyalty History

Customer Flight Activity

Calendar

Data Dictionary

Validated .head() and .shape().
<img width="1920" height="1080" alt="Screenshot (80)" src="https://github.com/user-attachments/assets/b4809f5c-d1e5-4155-8024-5dd6c66a2d04" />

🖼️ Image 4 — Dataset Shape & Overview

Confirmed:

16,737 loyalty members

392,936 flight records

Correct column structure
<img width="1920" height="1080" alt="Screenshot (81)" src="https://github.com/user-attachments/assets/c76e480a-dcba-4b87-b575-29ab667a804b" />

🖼️ Image 5 — Loyalty Dataset Preview

Reviewed:

Demographics

Enrollment year/month

Cancellation year/month

Salary

CLV
<img width="1920" height="1080" alt="Screenshot (82)" src="https://github.com/user-attachments/assets/514a74e4-fbcf-41a2-bbd8-d2df7839258b" />

🖼️ Image 6 — Flight Activity Preview

Reviewed:

Year

Month

Total Flights

Distance

Points Accumulated

Points Redeemed
<img width="1920" height="1080" alt="Screenshot (83)" src="https://github.com/user-attachments/assets/f11b9cca-376b-465c-9b20-a12fa19428e4" />

🖼️ Image 7 — Data Dictionary Inspection

Validated column definitions and descriptions.
<img width="1920" height="1080" alt="Screenshot (84)" src="https://github.com/user-attachments/assets/3a25e1a7-84bb-42bd-a6ab-9fb33aac8e98" />

🖼️ Image 8 — Data Types Check (info())

Verified:

Correct datatypes

Null counts

Memory usage
<img width="1920" height="1080" alt="Screenshot (85)" src="https://github.com/user-attachments/assets/f4c1cabf-c5af-4991-ab58-9431d99d9b66" />

🖼️ Image 9 — Missing Values Analysis

Findings:

Salary missing (~4,238)

Cancellation fields missing (~14,670, expected)

No structural issues
<img width="1920" height="1080" alt="Screenshot (86)" src="https://github.com/user-attachments/assets/457c0ec3-3137-4012-87c9-b70dba14bfb0" />

🖼️ Image 10 — Duplicate Check

Results:

Loyalty → 0 duplicates

Flight → acceptable monthly-level duplicates
<img width="1920" height="1080" alt="Screenshot (87)" src="https://github.com/user-attachments/assets/c52ea51d-efcc-46f3-9574-1b052a4aa0d9" />

🖼️ Image 11 — Column Cleaning

Standardized naming:

.lower()
.strip()
.replace(" ", "_")
<img width="1920" height="1080" alt="Screenshot (88)" src="https://github.com/user-attachments/assets/e219d55e-51be-472d-83ec-4a6db3ef9aab" />

🖼️ Image 12 — Enrollment Date Feature Engineering

Created:

enrollment_date


Converted year + month → datetime.
<img width="1920" height="1080" alt="Screenshot (89)" src="https://github.com/user-attachments/assets/16b7f0ec-cf59-4aa3-8e2c-6e5380deb979" />

🖼️ Image 13 — Campaign Period Classification

Defined campaign window:

Feb 2018 – Apr 2018


Created campaign_period:

pre_campaign

during_campaign

post_campaign
<img width="1920" height="1080" alt="Screenshot (90)" src="https://github.com/user-attachments/assets/985b91c4-5830-4d81-a4ef-5b01635ac15e" />

🖼️ Image 14 — Campaign Period Distribution

Customer counts:

Period	Members
Pre	13,919
During	971
Post	1,847
<img width="1920" height="1080" alt="Screenshot (91)" src="https://github.com/user-attachments/assets/2bb104d2-2048-4a57-8726-7f833a673826" />

🖼️ Image 15 — Cancellation Date + Active Flag

Created:

cancellation_date

is_active

Validated date logic.
<img width="1920" height="1080" alt="Screenshot (92)" src="https://github.com/user-attachments/assets/48cdd7c9-7d5e-4fda-85cf-6481df78e0ac" />

🖼️ Image 16 — Monthly Enrollment Aggregation

Grouped monthly enrollments.

Calculated:

Gross enrollments

Cancellations

Net membership change
<img width="1920" height="1080" alt="Screenshot (93)" src="https://github.com/user-attachments/assets/c0350a74-b616-45b4-8551-c2aed9a9626e" />

🖼️ Image 17 — Campaign vs Non-Campaign Averages

Average monthly enrollments:

Period	Avg
During Campaign	323
Outside Campaign	202

🔥 ~60% increase during campaign.
<img width="1920" height="1080" alt="Screenshot (94)" src="https://github.com/user-attachments/assets/d51f7a09-22a2-413f-9c77-fd9b7230dc90" />

🖼️ Image 18 — Monthly Enrollment Trend (Line Chart)

Visualized:

Monthly enrollments

Campaign shaded region

Clear spike visible.
<img width="1920" height="1080" alt="Screenshot (95)" src="https://github.com/user-attachments/assets/e1cf7144-0db6-4bb4-ba3f-5899aec1508d" />

🖼️ Image 19 — Cumulative Net Membership Growth

Plotted cumulative net members.

Strong upward trajectory.
<img width="1920" height="1080" alt="Screenshot (96)" src="https://github.com/user-attachments/assets/9b13cb7a-ec57-4527-a03e-089c8fa824a1" />

🖼️ Image 20 — Gender Adoption Analysis

Adoption rate by gender:

Minimal difference.

Campaign broadly neutral across genders.
<img width="1920" height="1080" alt="Screenshot (97)" src="https://github.com/user-attachments/assets/f99599ed-f040-4bab-a87c-41171d63b0ee" />

🖼️ Image 21 — Education Adoption Analysis

Adoption by education level:

Slightly higher for High School / Bachelor

Lower for Master / Doctor
<img width="1920" height="1080" alt="Screenshot (98)" src="https://github.com/user-attachments/assets/32aef230-abe3-4eac-84bf-1887271dba75" />

🖼️ Image 22 — Salary Band Creation

Segmented salary into:

<50K

50K–75K

75K–100K

100K+

Unknown

Prepared for adoption analysis.
<img width="1920" height="1080" alt="Screenshot (99)" src="https://github.com/user-attachments/assets/d7d49bf5-5d3c-4c21-9a46-371a80a8631c" />

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
<img width="1920" height="1080" alt="Screenshot (100)" src="https://github.com/user-attachments/assets/03a42696-0eb6-4ac1-8409-034e9196d605" />

🖼️ Image 24 — Summer Flight Filtering & Aggregation

Filtered:

May–August 2018

Grouped average flights by campaign_period.
<img width="1920" height="1080" alt="Screenshot (101)" src="https://github.com/user-attachments/assets/3f334133-7192-4532-8e04-4f575e12057c" />

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
<img width="1920" height="1080" alt="Screenshot (102)" src="https://github.com/user-attachments/assets/76b3862f-d9b7-4b13-98c6-22600be837ea" />

🛠 Tech Stack

Python

Pandas

NumPy

Matplotlib

Jupyter Notebook
