# 🚀 Credit Card Market Performance Dashboard 📊

**A Comprehensive Data Analytics Journey into Banking Sector Insights**

![Dashboard Overview](./images/dashboard_overview.png)
*Interactive Power BI Dashboard showcasing credit card market performance across multiple dimensions*

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Key Metrics & Performance](#key-metrics--performance)
- [Data Sources](#data-sources)
- [Dashboard Features](#dashboard-features)
- [Technical Implementation](#technical-implementation)
- [Banking Sector Analysis](#banking-sector-analysis)
- [Geographic Performance](#geographic-performance)
- [Temporal Trends](#temporal-trends)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [Key Insights](#key-insights)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [License](#license)

## 🔍 Project Overview

This interactive Power BI dashboard provides deep insights into the banking sector's credit card ecosystem by analyzing application trends across multiple dimensions. The project combines data from various sources to create a holistic view of market performance, helping stakeholders make data-driven decisions.

![Project Architecture](./images/project_architecture.png)
*Data flow and architecture diagram*

## 📈 Key Metrics & Performance

### Overall Performance Indicators
| Metric | Value | Growth Rate |
|--------|-------|-------------|
| **Total Applications** | 5,599 | 19.28% Monthly Growth |
| **Approved Applications** | 750 | 13.40% Approval Rate |
| **Rejected Applications** | 4,849 | 86.60% Rejection Rate |

![KPI Dashboard](./images/kpi_metrics.png)
*Key Performance Indicators visualization*

### Performance Breakdown
```
📊 Application Status Distribution:
├── Approved: 750 applications (13.40%)
└── Rejected: 4,849 applications (86.60%)

📈 Monthly Growth: 19.28%
🎯 Target Approval Rate: Industry benchmark comparison
```

## 🏦 Banking Sector Analysis

### Sector-wise Application Distribution

![Sector Analysis](./images/sector_distribution.png)
*Banking sector performance comparison*

| Sector | Applications | Market Share |
|--------|-------------|--------------|
| **Private Sector** | 2,893 | 51.7% |
| **Public Sector** | 1,632 | 29.1% |
| **Foreign Sector** | 1,074 | 19.2% |

### Major Banks Coverage
- **Public**: SBI, Bank of Baroda, Punjab National Bank
- **Private**: HDFC, ICICI, Kotak Mahindra, Axis Bank
- **Foreign**: Citibank, Standard Chartered, HSBC
- **Total Banks Analyzed**: 15+

## 🌍 Geographic Performance

### City-wise Approval Rates

![Geographic Performance](./images/geographic_heatmap.png)
*Geographic distribution of approval rates across major cities*

| City | Approval Rate | Performance Level |
|------|---------------|-------------------|
| **Kota** | 33.33% | 🟢 Excellent |
| **Connaught Place** | 26.56% | 🟡 Good |
| **Anantapur** | 20.31% | 🟡 Average |
| **Belgaum** | 20.31% | 🟡 Average |
| **Vasant Kunj** | 20.31% | 🟡 Average |

## 💳 Card Category Insights

### Card Type Distribution
![Card Categories](./images/card_type_distribution.png)
*Equal distribution across major card categories*

```
Card Type Distribution (800 each):
├── Gold Card: 800 applications
├── Master Card: 800 applications
├── Platinum Card: 800 applications
├── Rupay Card: 800 applications
└── Visa Card: 800 applications
```

### Co-brand Partnership Performance
![Co-brand Analysis](./images/cobrand_performance.png)
*Partnership performance across different brands*

| Co-brand Partner | Applications | Market Position |
|------------------|-------------|-----------------|
| **Amazon** | 464 | Market Leader |
| **Airtel** | Strong presence | Growing |
| **Flipkart** | Strong presence | Competitive |

## 📊 Temporal Trends

### Monthly Performance Analysis
![Monthly Trends](./images/monthly_trends.png)
*Time-series analysis showing seasonal patterns*

| Month | Approval Rate | Total Applications | Status |
|-------|---------------|-------------------|---------|
| **June** | 22.81% | Peak Performance | 🟢 |
| **July** | Declining | 2,306 (Highest Rejections) | 🔴 |
| **August** | Declining trend | Continued decline | 🟡 |

## 🔧 Technical Implementation

### DAX Formulas Used

#### Monthly Growth Calculation
```dax
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
```

#### Approval Rate Calculation
```dax
Approval_Rate = 
DIVIDE(
  CALCULATE(
    COUNTROWS(Dump),
    FILTER(Dump, Dump[Application_Status] = "Approved")
  ),
  [Total_Applications],
  0
)
```

#### Approved Applications Measure
```dax
Approved_App = 
CALCULATE(
  COUNTROWS(Dump),
  FILTER(Dump, Dump[Application_Status] = "Approved")
)
```

![DAX Implementation](./images/dax_formulas.png)
*Power BI DAX formula implementation examples*

## 🎯 Dashboard Features

### Interactive Components
- ✅ **Dynamic Filtering**: Bank Name, Card Type, and Sector filters
- ✅ **Time-series Analysis**: Month-wise trend analysis
- ✅ **Geographic Mapping**: Performance across different cities
- ✅ **Real-time KPI Monitoring**: Live performance indicators
- ✅ **Civil Score Distribution**: 52.8% vs 47.2% breakdown
- ✅ **Cross-sector Analysis**: Comparative performance metrics

![Dashboard Features](./images/dashboard_features.gif)
*Interactive dashboard features demonstration*

## 📊 Data Sources

The project integrates data from multiple sources:

| Source | Type | Usage |
|--------|------|-------|
| **ChatGPT** | AI Generated | Market insights and patterns |
| **Claude** | AI Generated | Analytical frameworks |
| **DeepSeek** | AI Generated | Deep learning insights |
| **Kaggle** | Public Datasets | Historical banking data |

## 🚀 Installation & Setup

### Prerequisites
- Microsoft Power BI Desktop
- Excel 2016 or later (for data preprocessing)
- Access to data sources (API keys if required)

### Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/credit-card-dashboard.git
   cd credit-card-dashboard
   ```

2. **Data Preparation**
   ```bash
   # Navigate to data folder
   cd data/
   # Run data preprocessing scripts
   python preprocess_data.py
   ```

3. **Open Power BI File**
   - Open `Credit_Card_Dashboard.pbix` in Power BI Desktop
   - Refresh data connections
   - Update data source paths if necessary

4. **Configure Data Sources**
   - Update connection strings in Power BI
   - Authenticate with required data sources
   - Test data refresh functionality

## 📈 Usage

### Viewing the Dashboard
1. Open the Power BI file
2. Use the navigation panel to explore different views
3. Apply filters to focus on specific segments
4. Export reports as needed

### Key Navigation Areas
- **Overview**: High-level KPI summary
- **Bank Analysis**: Sector and bank-wise performance
- **Geographic View**: Location-based insights
- **Temporal Analysis**: Time-series trends
- **Card Categories**: Product-wise breakdown

## 💡 Key Insights & Learnings

### Business Insights
- **Private Sector Dominance**: 51.7% market share indicates strong private banking presence
- **Geographic Variations**: Kota shows exceptional 33.33% approval rate
- **Seasonal Patterns**: June peak performance followed by decline
- **Card Type Balance**: Equal distribution suggests diverse market approach

### Technical Learnings
- **Data Integration**: Successfully merged multiple AI-generated and real datasets
- **Pattern Recognition**: Identified clear seasonal and geographic trends
- **Performance Optimization**: Efficient DAX formulas for real-time calculations
- **Visualization Best Practices**: Interactive and intuitive dashboard design

![Insights Summary](./images/key_insights.png)
*Visual summary of major business insights*

## 🛠️ Technologies Used

| Technology | Purpose | Version |
|------------|---------|---------|
| **Power BI Desktop** | Dashboard Creation | Latest |
| **DAX** | Data Analysis Expressions | - |
| **Excel** | Data Preprocessing | 2016+ |
| **Python** | Data Processing Scripts | 3.8+ |
| **SQL** | Data Querying | - |

## 📁 Project Structure

```
credit-card-dashboard/
├── README.md
├── Credit_Card_Dashboard.pbix
├── data/
│   ├── raw/
│   │   ├── applications_data.csv
│   │   ├── bank_details.csv
│   │   └── geographic_data.csv
│   ├── processed/
│   │   └── consolidated_data.csv
│   └── scripts/
│       └── preprocess_data.py
├── images/
│   ├── dashboard_overview.png
│   ├── kpi_metrics.png
│   ├── sector_distribution.png
│   └── monthly_trends.png
├── docs/
│   ├── data_dictionary.md
│   ├── dax_formulas.md
│   └── user_guide.md
└── assets/
    └── power_bi_template.pbit
```

## 🤝 Contributing

We welcome contributions to improve this dashboard! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/new-analysis`
3. **Make your changes and commit**: `git commit -m 'Add new geographic analysis'`
4. **Push to branch**: `git push origin feature/new-analysis`
5. **Submit a Pull Request**

### Contribution Guidelines
- Follow Power BI best practices
- Document new DAX formulas
- Include screenshots for UI changes
- Test dashboard functionality before submitting

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact & Support

- **Project Maintainer**: [Your Name](mailto:your.email@example.com)
- **LinkedIn**: [Your LinkedIn Profile](https://linkedin.com/in/yourprofile)
- **Issues**: [GitHub Issues](https://github.com/yourusername/credit-card-dashboard/issues)

## 🏷️ Tags

`#DataAnalytics` `#PowerBI` `#CreditCard` `#Banking` `#Dashboard` `#DAX` `#DataVisualization` `#FinTech` `#BusinessIntelligence` `#DataScience` `#Finance` `#MarketAnalysis`

---

⭐ **Star this repository if you found it helpful!** ⭐

![GitHub stars](https://img.shields.io/github/stars/yourusername/credit-card-dashboard)
![GitHub forks](https://img.shields.io/github/forks/yourusername/credit-card-dashboard)
![GitHub issues](https://img.shields.io/github/issues/yourusername/credit-card-dashboard)
![GitHub license](https://img.shields.io/github/license/yourusername/credit-card-dashboard)
