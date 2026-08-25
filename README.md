# Mexican Real Estate Market - Hands-On EDA

Hands-on exploratory analysis of the Mexican housing market to identify price drivers.

> WQU Data Science Lab DS 01 | ✅ Completed

### 1. Business Problem
What drives property prices in Mexico? Which states and property types are most expensive?

### 2. Dataset
- File: `mexico-real-estate-2.csv` (4,000+ listings)
- Target: `price_usd`
- Features: `state`, `lat`, `lon`, `property_type`, `surface_total`, `bedrooms`, `price_mxn`

### 3. What I Did (Detailed)

**A. Data Preparation**
- Currency: Validated `price_mxn` -> `price_usd` conversion
- Missing values: ~15% missing lat/lon, 10% missing surface - imputed median by state
- Outliers: Removed listings with price_per_m2 > 99th percentile
- Standardized: Cleaned state names (e.g., "Distrito Federal" -> "CDMX")

**B. EDA & Visualization**
- Distribution: `price_usd` is heavily right-skewed (log transform considered)
- Boxplots: Price by state - CDMX, Nuevo León, Quintana Roo highest median
- Scatter: `surface_total` vs `price_usd` (Pearson r ~0.6)
- Map: Folium/Scatter map of lat/lon colored by price_per_m2
- Property Type: Houses vs Apartments price comparison

**C. Feature Engineering**
- Created `price_per_m2 = price_usd / surface_total` for fair state comparison
- Created `price_per_room` feature
- Grouped analysis: Top 10 expensive municipalities

### 4. Key Findings
- Location is #1 driver: Coastal (Quintana Roo) and capital (CDMX) 2-3x higher price_per_m2 than inland states
- Size correlation is moderate and non-linear for luxury
- Data quality: Missing geo data biased towards cheaper rural listings

### 5. Tech Stack
Python, Pandas, NumPy, Matplotlib, Seaborn, Folium (optional)

### 6. How to Run
```bash
jupyter notebook notebook.ipynb