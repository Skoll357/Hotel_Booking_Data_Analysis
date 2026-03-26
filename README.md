# Hotel Booking Demand: Strategic Business Analysis (SQL)
# 📌 Project Overview
This project provides a comprehensive data-driven analysis of hotel booking demands using a dataset of 119,000+ records. By leveraging advanced SQL techniques, I diagnosed critical operational issues—such as a staggering **42% cancellation rate** at the City Hotel—and identified high-value customer segments to optimize revenue management and loss prevention strategies.
**Data Resource:https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand/data**

# 🎯 Business Objectives
**Loss Diagnosis**: Identify the "leakage points" in the booking funnel (Why do guests cancel?).
**Revenue Optimization**: Analyze Average Daily Rate (ADR) trends to identify high-margin markets.
**Customer Profiling**: Distinguish between "loyal" and "volatile" guest personas.
**Strategic Action**: Provide data-backed recommendations for City vs. Resort hotels.

# 🛠️ Tech Stack
**Database**: SQLite
**Environment**: VS Code (SQL Extension)
**Auxiliary Tools**: DB Browser for SQLite
**SQL Skills**: CTEs, Window Functions (ROW_NUMBER, RANK), Aggregate Functions

# 📈 Analysis Framework
The project is structured into four distinct phases:
**1. Loss Diagnosis (The "Leakage")**
Investigated why City Hotel faces a 42% cancellation rate.
Key Finding: Bookings made >180 days in advance have a 64% failure rate.
Insight: The "Non-Refundable" tag for Group bookings is often a trap, as these segments show systemic defaults.
**2. Revenue Mining (The "Gold")**
Identified which segments drive the most profit.
Key Finding: Direct and Online TA channels yield the highest ADR.
Insight: City Hotels thrive on "Last-Minute" demand, while Resort Hotels face "Perishable Inventory" issues where prices drop significantly as the check-in date nears.
**3. Customer Persona (The "Person")**
Differentiated guest behavior based on loyalty and social segments.
Key Finding: Repeated guests have a cancellation rate as low as 6.7% in Resort Hotels.
Insight: Families pay a 50% premium (higher ADR) but are more volatile in a resort setting compared to a city setting.
**4. Crown Jewel Ranking (The "Strategy")**
Developed a custom "Crown Score" (Volume×Success Rate×ADR) to rank the most valuable markets.
**Winner (City): FRA (France) Transient Guests** — Superior success rate (76%) and high ADR.
**Winner (Resort): PRT (Portugal) Transient Guests** — Mass-market volume driver.

# 💡 Key Strategic Recommendations
**City Hotel**: Implement a tiered deposit policy for bookings over 90 days and audit "Contract" segments which currently underperform in stability.
**Resort Hotel**: Focus on "Early Bird" incentives to lock in demand early and reduce reliance on last-minute price slashing. Enhance "Family" engagement to reduce their 36% cancellation risk.

# Project Structure
**data:**Stores the original dataset and cleaned intermediate products.
**sql:**Includes the complete SQL chain from cleaning and diagnostics to revenue analysis.
**scripts:**Python scripts for visualization generation.
**visuals:**Exported statistical charts (PNG/CSV).
**docs:**Final strategic analysis report and explanatory documents.

# 🚀 How to Run
1. Clone this repository.
2. Load the .csv file into a SQLite database using DB Browser for SQLite.
3. Run the scripts sequentially to reproduce the analysis.
4. The database address in the Python code is an absolute address; please change it manually at runtime.