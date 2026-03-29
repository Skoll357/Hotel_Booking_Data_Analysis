# 🏨 Hotel Booking Demand: Strategic Business Analysis (SQL)

## 📌 Project Overview
This project provides a comprehensive data-driven analysis of hotel booking demands using a dataset of **119,000+ records**. By leveraging advanced SQL techniques, I diagnosed critical operational issues—such as a staggering **42% cancellation rate** at City Hotels—and identified high-value customer segments to optimize revenue management and loss prevention strategies.

**Data Source:** [Kaggle - Hotel Booking Demand Dataset](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand/data)

---

## 🎯 Business Objectives
*   **Loss Diagnosis**: Identify the "leakage points" in the booking funnel (Why do guests cancel?).
*   **Revenue Optimization**: Analyze Average Daily Rate (ADR) trends to identify high-margin markets.
*   **Customer Profiling**: Distinguish between "loyal" and "volatile" guest personas.
*   **Strategic Action**: Provide data-backed recommendations for City vs. Resort hotels.

---

## 🛠️ Tech Stack & Skills
*   **Database**: SQLite (via DB Browser for SQLite)
*   **Analysis**: SQL (CTEs, Window Functions, Aggregate Functions, Data Binning)
*   **Visualization**: Python (Pandas, Matplotlib, Seaborn)
*   **Editor**: VS Code

---

## 📈 Analysis Framework
The project is structured into four distinct strategic phases:

### 1. Loss Diagnosis (The "Leakage")
Investigated the root causes of the high cancellation rate.
*   **Key Finding**: Bookings made **>180 days** in advance have a **64% failure rate**.
*   **Insight**: The "Non-Refundable" tag for Group bookings is often a trap; these segments show systemic defaults due to speculative blocking.

### 2. Revenue Mining (The "Gold")
Identified high-yield segments and pricing logic.
*   **Key Finding**: Direct and Online TA channels yield the highest ADR.
*   **Insight**: City Hotels thrive on **"Last-Minute Premiums"**, while Resort Hotels suffer from **"Perishable Inventory"** price slashing for late bookings.

### 3. Customer Persona (The "Person")
Differentiated guest behavior based on loyalty and social segments.
*   **Key Finding**: Repeated guests show a negligible cancellation rate of **6.7%** in Resort Hotels.
*   **Insight**: **Families** pay a **50% premium** (higher ADR) but are more volatile in a resort setting compared to a city setting.

### 4. Crown Jewel Ranking (The "Strategy")
Developed a custom **"Crown Score"** $(Volume \times Success\ Rate \times ADR)$ to rank the most valuable markets.
*   **Winner (City):** `FRA (France) - Transient` — Superior success rate (76%) and high ADR.
*   **Winner (Resort):** `PRT (Portugal) - Transient` — The undisputed mass-market volume driver.

---

## 💡 Strategic Recommendations

### 🏙️ City Hotel
*   **Tighten Cancellation Policies**: Implement mandatory non-refundable deposits for any booking with a Lead Time exceeding 90 days.
*   **Audit B2B Contracts**: Renegotiate terms with Offline Travel Agents and "Group" coordinators to reduce the 48%+ default rate.
*   **Capitalize on French Market**: Allocate a significant share of the marketing budget toward French transient travelers.

### 🏖️ Resort Hotel
*   **Stabilize Last-Minute Pricing**: Replace aggressive price slashing with "Value-Add" offers (e.g., free spa/dinner) to maintain ADR.
*   **Cultivate Family Segment**: Invest in family-centric amenities to increase the volume of this high-margin (+$60 premium) segment.
*   **British Anchor**: Deepen relationships with UK (GBR) agents; their **99.9% success rate** makes them perfect "occupancy fillers."

---

## 📂 Project Structure
```text
Hotel-Booking-Analysis/
├── data/                       # Original dataset and cleaned DB files
├── sql_code/                   # SQL scripts (Cleaning, Diagnosis, Revenue)
├── visualization_code/         # Python scripts for generating charts
├── output/                     # Exported charts (PNG) and data snippets
├── scripts/                    # Final Strategic Analysis Report (PDF/Word)
└── README.md                   # Project overview and documentation