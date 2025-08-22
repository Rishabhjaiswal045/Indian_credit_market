# 🚀 Credit Card Market Performance Dashboard Visualizing Performance with Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=power-bi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-FF6F00?style=for-the-badge&logo=microsoft&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)

## 🚀 Project Overview

A comprehensive Power BI dashboard that analyzes credit card application trends across banking sectors, providing deep insights into approval patterns, geographic performance, and temporal trends in the financial ecosystem.

**Project Link** - [Credit Card Market Performance Dashboard].(https://github.com/Rishabhjaiswal045/Indian_credit_market/edit/main/README.md)

## 📊 Key Metrics Tracked

🚀 Key Features
📈 Interactive KPI Monitoring: Track total applications, growth rate, and approval metrics in real-time.

🏦 Cross-Sector Analysis: Compare performance across Public, Private, and Foreign banking sectors.

🌍 Geographic Mapping: Visualize approval rates and application volumes across different cities.

⏰ Temporal Trend Analysis: Analyze month-wise performance and seasonal trends with time-series charts.

🔍 Advanced Filtering: Dynamically filter data by Bank Name, Card Type, Sector, and Date for granular analysis.

💳 Card Category Insights: Breakdown of performance by card type (Gold, Platinum, Visa, etc.) and co-branding partnerships.

📈 Dashboard Preview
(Note: You would replace the description below with an actual screenshot of your dashboard. Since I can't see it, I've described a common layout.)

The dashboard is organized into several key visual sections:

Top Banner: Key Metrics (Total Applications, Monthly Growth, Approved Apps, Approval Rate) displayed as dynamic cards.

Central Map: A geographic map of India color-coded by approval rate or application volume.

Trend Charts: Line charts showing application and approval trends over time (June-August).

Breakdown Charts: Bar and pie charts for Sector Performance, Card Type Distribution, and Bank-wise analysis.

Interactive Slicers: Filters on the side for user-driven exploration.

(Imagine a screenshot of your Power BI dashboard inserted here)

📋 Key Metrics & Insights
Metric	Value	Insight
Total Applications	5,599	Total volume of processed applications.
Monthly Growth Rate	19.28%	Significant month-over-month expansion in application volume.
Approval Rate	13.40%	Industry insights into application stringency.
Approved Applications	750	Successful applications.
Rejected Applications	4,849	Unsuccessful applications.
Top City by Approval	Kota (33.33%)	Geographic outlier with the highest success rate.
Sector-Wise Application Distribution
Private Sector: 2,893 applications (Market Leader)

Public Sector: 1,632 applications

Foreign Sector: 1,074 applications

Top Performing Cities (Approval Rate)
Kota: 33.33%

Connaught Place: 26.56%

Anantapur, Belgaum, Vasant Kunj: 20.31%

Card Type Distribution
Perfectly equal distribution across Gold, Master, Platinum, Rupay, and Visa (800 applications each).

Co-Branding Leaders
Amazon: 464 applications

Airtel & Flipkart: Strong market presence.

Temporal Trends
Peak Performance: June (22.81% approval rate)

Highest Rejections: July (2,306 applications)

Declining Trend: Observable dip in approval rates through July and August.

⚙️ Technical Implementation
Data Integration
Data was consolidated from multiple sources (#ChatGPT, #Claude, #DeepSeek, #Kaggle) into a unified model in Power BI.

Key DAX Formulas
1. Monthly Growth Calculation:

dax
Monthly_Growth =
VAR ThisMonth = [Total_Applications]
VAR LastMonth =
    CALCULATE(
        [Total_Applications],
        DATEADD(Dump[Login_Date], -1, MONTH)
    )
VAR Growth = DIVIDE(ThisMonth - LastMonth, LastMonth)
RETURN
    IF(ISERROR(Growth), 0, Growth)
2. Approval Rate Calculation:

dax
Approval_Rate =
DIVIDE(
    CALCULATE(
        COUNTROWS(Dump),
        FILTER(Dump, Dump[Application_Status] = "Approved")
    ),
    [Total_Applications],
    0
)
3. Approved Applications Measure:

dax
Approved_App =
CALCULATE(
    COUNTROWS(Dump),
    FILTER(Dump, Dump[Application_Status] = "Approved")
)
🎯 Insights & Learnings
Market Dominance: The Private Banking sector leads in application volume, indicating aggressive marketing or wider reach.

Geographic Disparity: Approval rates vary significantly by city, suggesting regional differences in creditworthiness or bank policies.

Seasonal Trends: The high rejection rate in July could indicate a shift in lending criteria or an influx of lower-quality applications.

Balanced Portfolio: The equal distribution of card type applications suggests a well-balanced market offering without a single dominant type.

🔮 Future Enhancements
Integrating real-time data feeds for live dashboard updates.

Predictive analytics to forecast application trends and approval likelihood.

Deeper customer segmentation analysis (e.g., by income, age, credit score).

- ✅ Additional data sources

## 🛠️ Technologies Used

- **Power BI** - Dashboard creation and visualization
- **DAX** - Data Analysis Expressions for calculations
- **Power Query** - Data transformation and modeling
- **Excel** - Source data preparation

## 📱 Dashboard Views

### Main Dashboard
- Executive summary with key KPIs
- Interactive filters and slicers
- Real-time data refresh

### Detailed Analytics
- Drill-down capabilities
- Category-wise performance
- Time-series analysis

### Profitability Analysis
- Product-level insights
- Margin analysis
- ROI calculations

---

## 📞 Contact

**Rishabh Jaiswal**
- GitHub: [@Rishabhjaiswal045](https://github.com/Rishabhjaiswal045)
- Project: [AirPods Dashboard](https://github.com/Rishabhjaiswal045/Indian_credit_market/edit/main/README.md)

---

*Built with ❤️ using Power BI and DAX*





