🚀Credit Card Market Performance Dashboard 📊
A Data Analytics Journey
I'm excited to share my latest project: a comprehensive Credit Card Market Performance Dashboard that provides deep insights into the banking sector's credit card ecosystem! 📊
🔍 #Project_Overview
This interactive Power BI dashboard analyzes credit card application trends across multiple dimensions, combining data from various sources including #ChatGPT, #Claude, #DeepSeek, and #Kaggle to create a holistic view of market performance.
📈 Key #Metrics & #Insights:
5,599 Total Applications processed
19.28% Monthly Growth rate
750 Approved Applications (13.40% approval rate)
4,849 Rejected Applications
🏦 #Banking_Sector Analysis:
Private Sector leads with 2,893 applications
Public Sector: 1,632 applications
Foreign Sector: 1,074 applications
Coverage across 15+ major banks (SBI, HDFC, ICICI, Kotak Mahindra, etc.)
🌍 #Geographic_Performance:
Kota shows highest approval rate at 33.33%
Connaught Place and other metro areas at 26.56%
Consistent 20.31% approval rates across Anantapur, Belgaum, and Vasant Kunj
💳 Card Category Insights:
Equal distribution across all major card types (Gold, Master, Platinum, Rupay, Visa - 800 each)
Amazon leads co-brand partnerships with 464 applications
Airtel and Flipkart showing strong market presence
📊 #Temporal_Trends:
Peak performance in June (22.81% approval rate)
Declining trend through July-August
July saw highest rejections (2,306 applications)
🔧 #Technical_Implementation:
Key DAX Formulas Used:
Monthly Growth Calculation:
daxMonthly_Growth = 
VAR ThisMonth = [Total_Applications]
VAR LastMonth = 
  CALCULATE(
    [Total_Applications],
    DATEADD(Dump[Login_Date], -1, MONTH)
  )
VAR Growth = DIVIDE(ThisMonth - LastMonth, LastMonth)
RETURN
  IF(ISERROR(Growth), 0, Growth)
Approval Rate Calculation:
daxApproval_Rate = 
DIVIDE(
  CALCULATE(
    COUNTROWS(Dump),
    FILTER(Dump, Dump[Application_Status] = "Approved")
  ),
  [Total_Applications],
  0
)
Approved Applications Measure:
daxApproved_App = 
CALCULATE(
  COUNTROWS(Dump),
  FILTER(Dump, Dump[Application_Status] = "Approved")
)
🎯 #Dashboard_Features:
✅ Interactive filtering by Bank Name, Card Type, and Sector
✅ Time-series analysis with month-wise trends
✅ Geographic performance mapping
✅ Real-time KPI monitoring
✅ Civil Score distribution analysis (52.8% vs 47.2%)
✅ Cross-sector comparative analysis
💡 Key Learnings:
Data Integration: Successfully merged datasets from multiple AI sources and platforms
Pattern Recognition: Identified seasonal trends in credit card applications
Market Insights: Private sector dominance with balanced card type distribution
Geographic Variations: Significant approval rate differences across cities
#DataAnalytics #PowerBI #CreditCard #Banking #Dashboard #DAX #DataVisualization #FinTech #BusinessIntelligence #DataScience #Finance #MarketAnalysis
