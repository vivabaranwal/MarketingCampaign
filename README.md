# Marketing Campaign & Customer Acquisition Analysis

## Overview
This project executes a comprehensive data science analysis of marketing campaign data using the **Marketing Mix (4Ps) framework**: Product, Price, Place, and Promotion. The analysis applies exploratory data analysis (EDA) and inferential statistical hypothesis testing to identify key socioeconomic and structural factors driving consumer purchasing behavior.

## Project Objectives
- **Data Audit & Validation**: Ensure structural integrity of datasets
- **Categorical Standardization**: Clean and standardize categorical fields
- **Feature Engineering**: Create meaningful derived variables
- **Exploratory Data Analysis**: Uncover patterns and distributions
- **Statistical Hypothesis Testing**: Test hypotheses about customer behavior
- **Customer Segmentation**: Identify high-value customer profiles
- **Marketing Insights**: Provide actionable recommendations based on 4Ps framework

## Project Structure
```
MarketingCampaign/
├── README.md                           # Project documentation
├── project.ipynb                       # Basic analysis notebook
├── project_theory.ipynb                # Comprehensive theoretical analysis
├── data/
│   ├── marketing_data.csv              # Main marketing dataset
│   └── Data Dictionary - Response to marketing campaigns.xlsx  # Data reference
└── venv/                               # Virtual environment
```

## Dataset
**File**: `data/marketing_data.csv`

**Key Variables**:
- **Customer Profile**: ID, Age (derived from Year_Birth), Education, Marital_Status, Income
- **Spending**: MntWines, MntFruits, MntMeatProducts, MntFishProducts, MntSweetProducts, MntGoldProds
- **Purchases**: NumWebPurchases, NumCatalogPurchases, NumStorePurchases
- **Engagement**: NumWebVisitsMonth, Response (to marketing campaigns)
- **Time**: Dt_Customer (registration date)
- **Demographics**: Kidhome, Teenhome (children in household)

## Installation & Setup

### Prerequisites
- Python 3.8+
- Jupyter Notebook/Lab
- pip or conda

### Environment Setup
```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install pandas numpy matplotlib seaborn scipy jupyter
```

## Usage

### Run the Analysis

**Option 1: Basic Project Analysis**
```bash
jupyter notebook project.ipynb
```
Covers data loading, cleaning, feature engineering, and initial visualizations.

**Option 2: Comprehensive Theoretical Analysis**
```bash
jupyter notebook project_theory.ipynb
```
Includes detailed EDA, 4Ps framework analysis, and statistical hypothesis testing.

## Key Analysis Steps

### 1. **Data Cleaning & Preparation**
- Strip whitespace from column headers
- Convert Income from string format ($X,XXX) to numeric
- Parse dates (Dt_Customer)
- Handle missing values using group-based median imputation

### 2. **Feature Engineering**
- Total Children = Kidhome + Teenhome
- Age = 2015 - Year_Birth
- Total Spending = Sum of all product categories
- Total Purchases = Sum of all purchase channels

### 3. **Categorical Standardization**
- Marital Status: Consolidate similar categories (e.g., 'Alone' → 'Single', 'YOLO' → 'Single')
- Education: Standardize education levels

### 4. **Exploratory Data Analysis**
- Distribution analysis (Income, Age, Spending)
- Outlier detection and treatment
- Cross-tabulations and relationships
- Visualization of key metrics

### 5. **Statistical Testing**
- Hypothesis testing on relationships between variables
- Significance analysis of customer segments
- Correlation studies

## Key Findings & Insights
(To be populated after analysis completion)

## Technologies Used
- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations
- **Matplotlib** - Data visualization
- **Seaborn** - Statistical data visualization
- **SciPy** - Statistical testing and analysis

## Author
**Viva Baranwal**

## License
This project is open source and available under the MIT License.

## Contact
For questions or feedback, please reach out via GitHub Issues.
