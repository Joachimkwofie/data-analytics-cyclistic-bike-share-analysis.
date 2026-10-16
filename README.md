# 🚲 Cyclistic Bike-Share Case Study 
> **Author:** Joachim Armookyi Kwofie  
> **Tools Used:** Google Sheets, Tableau Public, Git/GitHub  

---

## 📌 Project Overview
Cyclistic is a fictional bike-share company in Chicago with a fleet of over 5,800 bicycles and 600 docking stations. The company's marketing strategy relies heavily on building general brand awareness, but financial analysis reveals that **annual members are significantly more profitable than casual riders**.

The primary objective of this project is to analyze historical trip data to answer a core strategic question for executive leadership:  
> **How do annual members and casual riders use Cyclistic bikes differently?**

The resulting insights inform data-backed marketing strategies aimed at converting casual riders into long-term annual members.

---

## 📊 Summary of Data & Methodology

### 1. Data Cleaning & Preparation (Google Sheets)
* **Dataset:** Divvy/Cyclistic historical trip dataset containing **426,887 records**.
* **Calculated Fields Created:**
  * `ride_length`: Extracted trip durations (`ended_at - started_at`).
  * `day_of_week`: Mapped using `=WEEKDAY(started_at, 1)` where $1 = \text{Sunday}$ and $7 = \text{Saturday}$.
* **Data Cleaning & Anomaly Handling:**
  * Removed **290 extreme outlier rows** where ride duration exceeded 24 hours (caused by unreturned bikes or system/docking glitches).
  * Filtered out false starts and accidental unlocks lasting less than 1 minute (`< 00:01:00`).

### 2. Key Exploratory Findings
* **Commuters vs. Leisure Riders:**
  * **Annual Members:** Display high weekday trip volume (peaking mid-week at over 69k rides) with consistent, short durations (~11–13 minutes), indicating routine utilitarian commuting.
  * **Casual Riders:** Trip volumes peak heavily on weekends (~15k Sunday trips), with average durations ranging from **35 to 44 minutes** (~3.5× longer than member rides), indicating recreational and leisure use.

---

## 📈 Dashboard & Visualizations
An interactive dual-chart executive dashboard was built and published on **Tableau Public** to compare volume trends alongside ride durations:
* **Chart 1:** Side-by-Side Bar Chart — *Total Trip Volume by Day of Week*
* **Chart 2:** Side-by-Side Bar Chart — *Average Ride Duration by Day of Week (Minutes)*

🔗 **[View Interactive Tableau Public Dashboard](https://public.tableau.com/app/profile/joachim.kwofie/viz/CyclisticBike-ShareDataAnalysis-CapstoneProject/Dashboard1)

---

## 💡 Top Strategic Recommendations
1. **Weekend Pass Upgrade Incentive:** Launch targeted digital promotions allowing casual weekend riders to apply their single/day-pass cost as a discount toward an annual membership.
2. **Duration-Based Savings Messaging:** Deploy in-app prompts after long rides (>30 mins) showing casual users how much money they would save per month with an annual membership.
3. **Timed Sunday/Monday Retargeting:** Execute digital media ad campaigns on Sunday evenings and Monday mornings to convert weekend leisure riders right as their weekend activities conclude.
