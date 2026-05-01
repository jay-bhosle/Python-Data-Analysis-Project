# Northern Lights Air – Loyalty Campaign Impact Analysis  
**Python‑driven evaluation of a promotional campaign on enrollment, demographics, and flight behaviour**

## Project Overview
Northern Lights Air ran a targeted loyalty promotion from February to April 2018. This project analyses the campaign’s effectiveness in driving new memberships, which customer segments adopted it most, and whether campaign‑enrolled customers flew more during the following summer.

## Tools & Technologies
- **Python (pandas, numpy, matplotlib)** – Data loading, cleaning, feature engineering, statistical summaries, and visualisation  
- **Jupyter Notebook** – All analysis in a single, documented notebook

## Data Pipeline

### 1. Data Loading & Inspection
Loaded four CSVs (Loyalty History, Flight Activity, Calendar, Data Dictionary) and examined shapes, data types, and missing values.  
<img width="1920" height="1080" alt="Screenshot (78)" src="https://github.com/user-attachments/assets/1e435a2b-fa36-4e23-9d72-f05d528c3b31" />  
<img width="1920" height="1080" alt="Screenshot (79)" src="https://github.com/user-attachments/assets/fde594b9-adeb-46fd-8dba-9b7c7fedae97" />  
<img width="1920" height="1080" alt="Screenshot (81)" src="https://github.com/user-attachments/assets/9de9086a-072c-42b0-ab37-1b2f1fadc455" />

### 2. Data Cleaning & Feature Engineering
Standardised column names, created proper `enrollment_date` and `cancellation_date` fields, and tagged each member’s enrollment relative to the campaign period.  
<img width="1920" height="1080" alt="Screenshot (86)" src="https://github.com/user-attachments/assets/56781a7e-686f-43ba-949b-7146fccf65cc" />  
<img width="1920" height="1080" alt="Screenshot (87)" src="https://github.com/user-attachments/assets/83e4ac8f-fef6-4b05-9fb2-baa90eddfccb" />

### 3. Trend & Adoption Analysis
Aggregated monthly gross enrollments and net membership change, then compared campaign months against the rest. Merged demographic data to calculate adoption rates by gender, education, and salary band.  
<img width="1920" height="1080" alt="Screenshot (91)" src="https://github.com/user-attachments/assets/309d809c-a877-475d-a32e-3cd05837366c" />  
<img width="1920" height="1080" alt="Screenshot (92)" src="https://github.com/user-attachments/assets/2a12a4d1-7d87-41b4-8b42-25b5f04c4f57" />  
<img width="1920" height="1080" alt="Screenshot (95)" src="https://github.com/user-attachments/assets/895f458b-60e7-4438-b191-3e25dcb23f00" />

### 4. Summer Flight Behaviour
Joined cleaned flight activity with loyalty history, filtered for May–August 2018, and compared average flights for members who joined pre‑, during, and post‑campaign.  
<img width="1920" height="1080" alt="Screenshot (101)" src="https://github.com/user-attachments/assets/e6caec55-5b2b-432f-b559-2c803dda1323" />

## Key Insights

- **Campaign drove significant enrollment uplift**  
  During the campaign (Feb–Apr 2018), average monthly gross enrollments rose to **324**, compared to **202** in non‑campaign months – a **60% increase**.

- **Net membership growth was entirely positive**  
  All campaign months showed positive net change, indicating the promotion attracted stickier members.

- **Demographic adoption was broad, with slight female skew**  
  – **Gender:** Females adopted at a rate of **5.87%** vs. **5.73%** for males – a marginal difference.  
  – **Salary:** Lower‑income earners (<$50K) adopted at **16.0%** – nearly three times higher than any other band. The “Unknown” group (likely non‑responders) followed with **6.1%**.

- **Campaign joiners flew more in summer 2018**  
  Members who enrolled **during the campaign** averaged the highest number of flights in May–August 2018, outperforming both pre‑campaign and post‑campaign cohorts. This indicates the campaign attracted genuinely active travellers.

## Recommendations
- **Retain high‑value Loyalty members** – Focus incentives on customers with the highest flight activity and lifetime value to prevent revenue loss.  
- **Re‑engage inactive but previously loyal customers** – Use personalised win‑back offers for members with strong past activity who recently disengaged.  
- **Personalise rewards by Loyalty tier** – Align benefits to tier behaviour instead of one‑size‑fits‑all promotions.  
- **Incentivise flight frequency, not just distance** – Reward frequent flyers to encourage habitual travel and strengthen long‑term loyalty.  
- **Use behaviour trends to predict and prevent churn** – Monitor declining activity and trigger early retention campaigns before customers disengage.

<img width="1920" height="1080" alt="Screenshot (102)" src="https://github.com/user-attachments/assets/0069ce1f-a3b7-4aec-9349-123c6249b975" />
