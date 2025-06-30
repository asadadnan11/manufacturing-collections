# Manufacturing Collections Optimization

## Executive Summary

This class project simulates optimizing collections processes for a manufacturing company using synthetic data to reflect real-world payment behaviors.

This project simulates a collections optimization initiative for a large appliance manufacturing company, demonstrating analytics and machine learning techniques to improve accounts receivable management. Using synthetic data that reflects realistic payment behaviors and industry patterns, the analysis explores how data-driven approaches can improve cash flow and reduce financial risk.

The project combines traditional financial analysis with predictive modeling to deliver insights for collections strategy optimization. This work was completed as part of a graduate-level business analytics course, focusing on practical application of statistical methods to real-world business challenges.

## Business Objective

**Primary Goal**: Explore the potential to reduce Days Sales Outstanding (DSO) and improve collections prediction accuracy to accelerate cash flow and minimize bad debt exposure.

**Project Learning Objectives**:
- Analyze current DSO performance against industry benchmarks (40-day standard)
- Develop predictive models to identify late payment probability
- Create risk-based customer segmentation framework
- Generate data-driven insights for collections strategy optimization
- Demonstrate practical application of machine learning in finance operations

## Key Features

### Data Generation & Simulation
- **Synthetic Dataset**: 1,000 realistic invoices across 500 customers
- **Comprehensive Attributes**: Invoice amounts, payment terms, due dates, payment behaviors
- **Realistic Patterns**: Industry-typical payment distributions, seasonal variations, and customer risk profiles
- **Payment Scenarios**: On-time, late, and unpaid invoices reflecting real-world collection challenges

### Advanced Data Processing
- **Missing Payment Handling**: Sophisticated logic for unpaid invoice management
- **DSO Calculations**: Industry-standard metrics with benchmark comparisons
- **Risk Categorization**: Multi-tier customer risk assessment (No Risk, Low Risk, Medium Risk, High Risk)
- **Feature Engineering**: Customer payment history, seasonal patterns, and amount-based risk factors

### Baseline Performance Analysis
- **Industry Benchmarking**: Comparison against 40-day appliance manufacturing standard
- **Segmentation Analysis**: Performance breakdown by credit terms, invoice amounts, and customer categories
- **Trend Identification**: Monthly and quarterly payment pattern analysis
- **Collection Efficiency**: Comprehensive rate calculations and performance metrics

### Advanced Predictive Modeling
- **Logistic Regression**: Statistical foundation for understanding payment behavior drivers
- **XGBoost Implementation**: Gradient boosting for superior prediction accuracy
- **Model Comparison**: Performance evaluation showing 18% accuracy improvement
- **Feature Importance**: Data-driven insights into key late payment predictors

### Comprehensive Visualizations
- **Payment Risk Distribution**: Clear visualization of customer risk categories
- **DSO Performance Trends**: Monthly and credit-term-based performance analysis
- **Model Performance Comparison**: ROC curves and accuracy metrics
- **Customer Segmentation**: Risk profile distributions and payment behavior patterns

### Business Intelligence Integration
- **Power BI Ready**: Four export-ready CSV files for dashboard creation
- **Executive Reporting**: Summary statistics and KPI tracking
- **Customer Profiles**: Individual risk assessments and payment histories
- **Model Predictions**: Real-time risk scoring for operational deployment

## Project Results & Learning Outcomes

### Model Performance Achieved:
- **DSO Analysis**: Current performance ~15% above industry benchmark (40 days)
- **Prediction Models**: XGBoost achieved 0.856 AUC (18% improvement over logistic regression baseline)
- **Risk Segmentation**: 89% accuracy in customer risk categorization
- **Collection Analysis**: 94% overall collection rate identified across paid invoices

### Key Business Insights Discovered:
- **High-Value Invoice Risk**: 23% higher late payment probability for invoices >$15,000
- **Credit Terms Impact**: 60-day terms correlate with 31% higher DSO than 30-day terms  
- **Predictive Features**: Historical payment behavior emerged as strongest predictor
- **Seasonal Patterns**: Q4 shows 12% increase in collection delays (holiday effect)

### Challenges Encountered & Solutions:
- **Data Quality**: Initial synthetic dataset required iterative refinement for realistic patterns
- **Feature Selection**: Tested multiple approaches before settling on customer history + invoice characteristics
- **Model Overfitting**: Early models showed 95%+ accuracy - had to balance complexity vs. realism
- **Class Imbalance**: Late payment minority class required stratified sampling techniques

### Project Limitations:
- Analysis limited to synthetic data - real-world validation needed
- 12-month timeframe may not capture all seasonal variations
- Customer behavior assumptions based on literature review vs. industry data
- Model performance estimates may not generalize to different business contexts

## How to Run

### Prerequisites
```bash
# Python 3.8+ required
pip install pandas numpy matplotlib seaborn scikit-learn xgboost jupyter
```

### Installation Steps
1. **Clone the Repository**
   ```bash
   git clone https://github.com/asadadnan11/manufacturing-collections.git
   cd manufacturing-collections
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

4. **Open and Run**
   - Open `manufacturing-collections.ipynb`
   - Run all cells sequentially (Cell → Run All)
   - Analysis will generate visualizations and export CSV files

### Expected Outputs
- **Visualizations**: Comprehensive charts and graphs displayed in notebook
- **CSV Exports**: Four files ready for Power BI integration
- **Model Results**: Performance metrics and predictions
- **Business Insights**: Executive summary and recommendations

## Sample Visuals

### DSO Performance by Credit Terms
![DSO by Credit Terms](images/dso_by_credit_terms.png)
*Days Sales Outstanding performance analysis compared to industry benchmark of 40 days*

### Model Performance Comparison
![Model Performance Comparison](images/model_performance_comparison.png)
*XGBoost significantly outperforms Logistic Regression in both accuracy and AUC-ROC metrics*

### Monthly DSO Trends
![Monthly DSO Trends](images/monthly_dso_trends.png)
*Seasonal patterns in payment behavior with clear quarterly variations*

## Project Structure

```
manufacturing-collections/
├── manufacturing-collections.ipynb    # Main analysis notebook
├── README.md                         # This file
├── LICENSE                          # MIT License
├── requirements.txt                 # Python dependencies
├── images/                          # Visualization images
│   ├── dso_by_credit_terms.png
│   ├── model_performance_comparison.png
│   └── monthly_dso_trends.png
└── exports/                         # Generated CSV files
    ├── manufacturing_collections_main_data.csv
    ├── customer_risk_profiles.csv
    ├── executive_summary_metrics.csv
    └── model_performance_comparison.csv
```

## Implementation Recommendations

### Phase 1: Pilot Program (Months 1-3)
1. **Model Validation**: Test predictive models on 6-month historical data subset
2. **Risk Score Integration**: Implement scoring for 100 highest-value customers
3. **Dashboard Development**: Create initial Power BI prototype for collections team
4. **Process Documentation**: Establish workflows and training materials

### Phase 2: Scaled Implementation (Months 4-9)
1. **Full Model Deployment**: Extend risk scoring to all active customers
2. **Credit Policy Updates**: Adjust terms based on customer risk profiles
3. **Collections Workflow**: Implement risk-based priority queues
4. **Performance Monitoring**: Establish monthly tracking and reporting

### Phase 3: Optimization (Months 10-12)
1. **Model Refinement**: Retrain with actual performance data
2. **Process Automation**: Integrate with existing CRM/ERP systems
3. **Continuous Improvement**: Establish quarterly review cycles

### Estimated Business Impact
- **Implementation Cost**: $125K-175K (staff time, system integration, training)
- **Projected Annual Savings**: $300K-450K (reduced DSO, lower bad debt)
- **Expected ROI**: 240-320% over 18 months
- **Break-even Timeline**: 8-12 months post-implementation

### Academic Validation Needed
- **Real Data Testing**: Validate model performance on actual customer data
- **A/B Testing**: Compare predictive vs. traditional collection approaches
- **Longitudinal Study**: Track 12+ month outcomes for full seasonal cycle

## Technical Approach

### Data Science Methodology
- **Synthetic Data Generation**: Realistic simulation of manufacturing payment patterns
- **Feature Engineering**: Customer history, seasonal patterns, and risk indicators
- **Model Selection**: Comparative analysis of statistical and machine learning approaches
- **Validation**: Cross-validation and performance testing for robust results

### Business Intelligence
- **KPI Development**: Industry-standard metrics with customized insights
- **Visualization Design**: Executive-friendly charts and operational dashboards
- **Export Optimization**: Power BI-ready data formats and structures

## Academic Disclaimer

This is a **graduate-level coursework project** using **synthetic data** generated to simulate realistic manufacturing payment patterns. All results, insights, and recommendations are for **educational purposes only** and represent learning outcomes from a business analytics program.

While the methodologies and analytical approaches follow industry standards, the specific numerical results should not be considered as actual business performance indicators. The project demonstrates practical application of data science techniques learned in coursework and serves as a portfolio piece for academic and professional development.

**Note**: This work was completed as part of graduate studies in business analytics. Any implementation would require validation with real data and appropriate business context.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

This project represents coursework from a graduate business analytics program. Feel free to fork, modify, and enhance the analysis for your own learning and development purposes. Suggestions for improvement or alternative analytical approaches are welcome as part of the ongoing learning process.

---

**Built with**: Python, Pandas, Scikit-learn, XGBoost, Matplotlib, Seaborn, Jupyter

**Asad Adnan** 
