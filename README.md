# PhonePe 2024 Data Dashboard

A comprehensive data visualization and analysis dashboard for PhonePe transaction data from 2024. This project processes, analyzes, and visualizes digital payment trends and patterns across India's digital payment ecosystem.

## 📊 Overview

This dashboard provides insights into:
- Transaction volumes and trends throughout 2024
- Payment patterns across different regions and demographics
- Digital payment adoption metrics
- Transaction value analysis
- User engagement patterns

## 🖼️ Dashboard Screenshots

### Main Dashboard View
![Dashboard Overview](phonpe%20dasboard/assests/Screenshot%202026-07-14%20142155.png)

### Transaction Analytics
![Transaction Analytics](phonpe%20dasboard/assests/Screenshot%202026-07-14%20142513.png)

### Regional Analysis
![Regional Analysis](phonpe%20dasboard/assests/Screenshot%202026-07-14%20142537.png)

### Payment Methods Breakdown
![Payment Methods](phonpe%20dasboard/assests/Screenshot%202026-07-14%20142607.png)

## 📁 Project Structure

```
phonpe dasboard/
├── DataSet_Source/          # Raw and processed data files
│   └── *.csv               # Transaction data organized by regions and time periods
│
├── assests/                  # Dashboard screenshots and visual resources
│   ├── Screenshot 2026-07-14 142155.png
│   ├── Screenshot 2026-07-14 142513.png
│   ├── Screenshot 2026-07-14 142537.png
│   └── Screenshot 2026-07-14 142607.png
│
└── Application Files        # Main dashboard application files
    ├── app.py              # Main Streamlit application
    └── analysis.py         # Data analysis scripts
```

## 🛠️ Tech Stack

- **Data Analysis**: Python (Pandas, NumPy)
- **Visualization**: Streamlit / Plotly / Matplotlib
- **Data Processing**: Python scripts for ETL
- **Data Format**: CSV datasets

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/GOD694/PhonePe_2024_data_dashboard.git
cd PhonePe_2024_data_dashboard
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required dependencies:
```bash
pip install pandas numpy streamlit plotly matplotlib
```

### Running the Dashboard

For Streamlit-based dashboard:
```bash
cd "phonpe dasboard"
streamlit run app.py
```

Or run analysis scripts directly:
```bash
python analysis.py
```

## 📊 Data Structure

The `DataSet_Source` directory contains:
- **Transaction Data**: CSV files with complete transaction records
- **Regional Breakdowns**: Payment data segmented by geographic regions
- **Demographic Segmentation**: User-based transaction analysis
- **Time Series Data**: Hourly, daily, and monthly aggregations
- **Payment Type Classification**: UPI, Cards, Wallets, Bank Transfers, etc.

## 📈 Features

### Interactive Visualizations
- Explore payment trends with interactive charts
- Drill-down capabilities for detailed analysis
- Real-time filtering and sorting
- Export capabilities for reports

### Regional Analysis
- Transaction patterns across different regions
- State-wise and city-wise breakdowns
- Regional growth comparison
- Top performing regions identification

### Time Series Analysis
- Track changes and trends throughout 2024
- Seasonal and cyclical pattern detection
- Month-over-month and year-over-year comparisons
- Anomaly detection for unusual patterns

### Payment Method Analysis
- Distribution across UPI, cards, wallets
- Method-wise transaction volume trends
- Payment method adoption rates
- Average transaction values by method

### User Demographics
- Payment behavior across age groups
- Gender-wise transaction patterns
- User engagement metrics
- Customer lifetime value analysis

## 📝 Usage Examples

### Basic Analysis
```python
import pandas as pd

# Load the data
df = pd.read_csv('phonpe dasboard/DataSet_Source/transactions.csv')

# Basic statistics
print(df.describe())
print(df.info())

# Top 10 transactions
print(df.nlargest(10, 'amount'))
```

### Regional Analysis
```python
# Analyze by region
regional_stats = df.groupby('region').agg({
    'amount': ['sum', 'mean', 'count'],
    'user_id': 'nunique'
}).round(2)

print(regional_stats)
```

### Time Series Visualization
```python
import matplotlib.pyplot as plt

# Plot daily transaction volume
daily_volume = df.groupby('date')['amount'].sum()
daily_volume.plot(figsize=(14, 6))
plt.title('Daily Transaction Volume - 2024')
plt.xlabel('Date')
plt.ylabel('Amount (₹)')
plt.grid(True, alpha=0.3)
plt.show()
```

### Payment Method Distribution
```python
# Payment method analysis
payment_dist = df['payment_method'].value_counts()
payment_dist.plot(kind='pie', autopct='%1.1f%%', figsize=(10, 8))
plt.title('Payment Method Distribution')
plt.show()
```

## 🔍 Key Metrics

The dashboard tracks:

| Metric | Description |
|--------|-------------|
| Total Transaction Volume | Sum of all transactions processed |
| Total Transaction Value | Total amount transferred (in ₹) |
| Average Transaction Amount | Mean transaction value |
| Active Users | Unique users making transactions |
| Transaction Growth Rate | Month-over-month percentage change |
| Top Regions | Best performing geographic areas |
| Peak Transaction Hours | Time periods with highest activity |

## 🎯 Analysis Insights

- **Seasonal Trends**: Payment volume spikes during festivals and shopping seasons
- **Regional Leaders**: Identify top performing states and cities
- **User Behavior**: Understand transaction patterns and preferences
- **Payment Preferences**: Track adoption of different payment methods
- **Growth Metrics**: Monitor overall digital payment ecosystem growth

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

## 📋 Contribution Guidelines

- Ensure code follows PEP 8 standards
- Add comments for complex logic
- Update documentation for new features
- Include test cases for data processing functions

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

- **GOD694** - [GitHub Profile](https://github.com/GOD694)

## 📞 Support & Feedback

For issues, questions, or suggestions:
- Open an [Issue](https://github.com/GOD694/PhonePe_2024_data_dashboard/issues)
- Submit feature requests
- Provide feedback on visualizations

## 🔗 Resources & References

- [PhonePe Official](https://www.phonepe.com/)
- [Streamlit Documentation](https://docs.streamlit.io/)
- [Plotly Charts](https://plotly.com/python/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Python Data Analysis Guide](https://www.freecodecamp.org/)

## 📅 Version History

- **v1.0** (July 2026) - Initial release with 2024 data analysis
  - Complete transaction dataset analysis
  - Interactive dashboard with 4 main views
  - Regional and demographic breakdowns
  - Time series trend analysis

## 🔐 Data Privacy & Disclaimer

- This dashboard analyzes aggregated PhonePe transaction data
- No personal or sensitive information is exposed
- All data is anonymized and aggregated
- For latest official data, refer to PhonePe reports

## 📞 Quick Links

- [Report an Issue](https://github.com/GOD694/PhonePe_2024_data_dashboard/issues/new)
- [Start a Discussion](https://github.com/GOD694/PhonePe_2024_data_dashboard/discussions)
- [View Pull Requests](https://github.com/GOD694/PhonePe_2024_data_dashboard/pulls)

---

**Last Updated**: July 2026

**Note**: This dashboard analyzes 2024 PhonePe transaction data with comprehensive visualizations and insights into India's digital payment landscape.
