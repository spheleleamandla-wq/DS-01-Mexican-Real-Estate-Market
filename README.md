# DS 01: Hands-on Data Science in the Mexican Real Estate Market

# Mexican Real Estate Market - Hands-On EDA

## Project Overview
This project focuses on applying hands-on data science techniques to analyze and understand trends in the Mexican real estate market.


Exploratory analysis of the Mexican housing market to identify what drives property prices.

> WorldQuant University - Data Science Lab DS 01 | Status: ✅ Completed

### Business Question
What are the price trends and key drivers in the Mexican real estate market?

### Dataset
- `mexico-real-estate` dataset (4,000+ listings)
- Features: state, lat/lon, property_type, price_usd, surface, bedrooms

### What I Did

**1. Data Cleaning**
- Cleaned with Pandas: fixed `price_mxn` -> `price_usd` conversion, handled missing lat/lon, removed price outliers > 99th percentile
- Standardized `state` names

**2. EDA & Visualization**
- Histograms: Highly skewed price distribution
- Boxplots: Price by state - CDMX, Nuevo León, Quintana Roo are highest
- Scatter + Maps: Relationship between surface area and price, geo-distribution of listings

**3. Analysis**
- Calculated price_per_m2 to compare markets fairly
- Pearson correlation: surface vs price = ~0.6 (moderate)
- Grouped analysis: Top 5 most expensive states/municipalities

### Key Findings
- **Location is key:** Coastal and capital states have 2-3x higher price_per_m2
- **Size matters but not linear:** Correlation between total surface and price breaks down for luxury segment
- **Data Quality Insight:** ~15% of listings missing coordinates - impacted mapping analysis

### Tech Stack
`Python` `Pandas` `Matplotlib` `Seaborn` `EDA`

### Files
- `notebook.ipynb` - Full analysis
- `data/` - Raw CSV

### How to Run
```bash
pip install pandas matplotlib seaborn
jupyter notebook notebook.ipynb



## Key Areas
- Data collection and cleaning
- Exploratory data analysis (EDA)
- Statistical analysis
- Data visualization
- Market insights and recommendations

## Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebooks

## Project Structure
```
DS-01-Mexican-Real-Estate-Market/
├── README.md
├── data/
├── notebooks/
├── scripts/
└── results/
```


## Author
spheleleamandla-wq

## License
MIT License
