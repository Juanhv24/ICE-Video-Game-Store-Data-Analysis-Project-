# 🎮 ICE — Video Game Store (Data Analysis Project)

## 📘 Project Overview
This project analyzes **video game sales, ratings, and platform trends** for the fictional online store **ICE**.  
The dataset `games.csv` contains information such as game titles, release years, genres, critic/user scores, ESRB ratings, and sales in different regions.

The main goal is to **identify patterns that determine game success** and to **forecast potential sales for 2017**, based on data available up to 2016.

---

## 🧩 Dataset Information

**File:** `/datasets/games.csv`  
**Columns:**
- `Name` — Game title  
- `Platform` — Console/platform (e.g., PS4, Xbox One)  
- `Year_of_Release` — Year game was released  
- `Genre` — Game genre (Action, Sports, etc.)  
- `NA_sales`, `EU_sales`, `JP_sales`, `Other_sales` — Regional sales (millions of USD)  
- `Critic_Score` — Average critic rating (0–100)  
- `User_Score` — Average user rating (0–10; may include `TBD`)  
- `Rating` — ESRB rating (E, T, M, etc.)

---

## 🧠 Project Objectives

1. **Data Cleaning & Preparation**
   - Standardize column names and data types.
   - Handle missing values and special cases (`TBD`).
   - Remove duplicates and fix inconsistent labels.
   - Create new calculated features like `total_sales`.

2. **Exploratory Data Analysis (EDA)**
   - Examine data distribution and trends by year, platform, and genre.
   - Analyze relationships between critic/user scores and sales.
   - Compare sales across regions (NA, EU, JP, Others).
   - Identify best-selling platforms and genres.

3. **Statistical Analysis**
   - Test hypotheses about score differences and sales relationships.
   - Evaluate whether user or critic scores better predict sales.
   - Analyze correlation and statistical significance using **SciPy** and **Statsmodels**.

4. **Forecasting 2017 Sales**
   - Build a simple predictive model using **scikit-learn** (e.g., linear regression or decision tree).
   - Estimate which platforms and genres will perform best in 2017.
   - Visualize results and key drivers of predicted performance.

5. **Visualization & Storytelling**
   - Create clear, well-labeled plots with **Matplotlib**, **Seaborn**, and **Plotly**.
   - Build storytelling markdown cells describing findings and implications.
   - (Optional) Create a simple interactive dashboard using **Streamlit**.

6. **Project Documentation**
   - Record cleaning decisions and data dictionary.
   - Save final cleaned dataset (`games_clean.csv`, `games_clean.parquet`).
   - Export profiling reports and summary visualizations.
   - Write conclusions and recommendations for marketing or inventory decisions.

---

## 🧰 Tools and Libraries

| Category | Packages |
|-----------|-----------|
| Data Wrangling | `pandas`, `numpy`, `pyjanitor`, `pyarrow` |
| Visualization | `matplotlib`, `seaborn`, `plotly` |
| Statistics & Modeling | `scipy`, `statsmodels`, `scikit-learn`, `category-encoders` |
| Profiling & Quality | `ydata-profiling` |
| I/O & Utilities | `openpyxl`, `python-dateutil`, `fastparquet` |
| Environment & Reproducibility | `jupyterlab`, `black`, `isort`, `flake8`, `tqdm`, `rich`, `python-dotenv` |

---

## 🪜 Project Plan (Step-by-Step)

### 1. Import & Inspect
- Load `games.csv` using pandas with predefined `na_values`.
- Check structure, dimensions, and missing values.
- Preview data for anomalies or encoding issues.

### 2. Data Cleaning
- Convert all column names to lowercase (`snake_case`).
- Trim whitespace, fix inconsistent platform/genre names.
- Convert types:
  - `year_of_release` → integer  
  - `sales columns` → float  
  - `critic_score` (0–100), `user_score` (0–10)
- Replace “TBD” with `NaN` and handle missing data.
- Remove duplicates and check for valid ranges.
- Compute `total_sales` and validate integrity.

### 3. Exploratory Data Analysis (EDA)
- Distribution of games released per year.
- Total sales per platform and genre.
- Regional sales patterns (NA vs EU vs JP).
- Correlation between scores and sales.
- Identify trends over time and platform life cycles.

### 4. Statistical Testing
- Compare average user and critic scores.
- Evaluate score differences between platforms.
- Test significance using **Mann–Whitney U**, **Kruskal–Wallis**, or **t-tests** as appropriate.

### 5. Forecasting 2017
- Aggregate sales by platform/genre (2013–2016).
- Train a simple regression model to predict total sales.
- Evaluate model performance (MAE, R²).
- Identify top potential platforms/genres for 2017.

### 6. Visualization & Reporting
- Create polished plots (sales trends, score vs sales scatter, boxplots).
- Summarize insights in Markdown storytelling.
- Generate a `report.pdf` or `README_summary.md` for presentation.

---

## 📊 Expected Outcomes

- Identification of top-performing platforms and genres.
- Insights on the influence of critic vs user scores on sales.
- Predictive outlook for 2017 game market trends.
- Recommendations for marketing and production strategies.

---

## 🧑‍💻 Author

**Juan Daniel Hernández Vargas**  
Data Scientist | Biologist | TripleTen Student  
📍 Colombia  
💼 [LinkedIn](https://www.linkedin.com) *(add your link)*# ICE-Video-Game-Store-Data-Analysis-Project-