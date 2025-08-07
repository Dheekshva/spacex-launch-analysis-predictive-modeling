
---

## Problem Statement

SpaceX is trying to reduce launch costs by making landings successful and reusable. This project aims to:
- Understand the factors influencing launch success.
- Perform EDA on launch data using SQL and visualizations.
- Build machine learning models to predict launch success based on payload, orbit, booster version, etc.

---

## Tools & Technologies

- **Languages**: Python 3
- **Data Analysis**: Pandas, Numpy
- **Visualization**: Matplotlib, Seaborn, Plotly, Folium
- **SQL**: SQLite
- **Dashboard**: Dash (Plotly Dash)
- **Machine Learning**: Scikit-Learn
- **IDE**: JupyterLab

---

## Datasets Used

- `dataset_part_1.csv`: Historical launch records (success/failure)
- `dataset_part_2.csv`: Feature data for ML modeling
- `dataset_part_3.csv`: Labels for ML modeling
- Data was collected from the [SpaceX REST API](https://api.spacexdata.com) and from public CSV files provided in the IBM capstone course.

---

## Project Highlights

### 1. Data Collection & Wrangling
- Collected data using SpaceX REST API and CSV datasets
- Cleaned missing values, unified datatypes, and removed irrelevant features

### 2. Exploratory Data Analysis (EDA)
- Plotted bar charts, pie charts, and scatter plots to explore trends in:
  - Launch success rates
  - Booster versions
  - Payload mass
- Used SQL queries to summarize success rates by orbit, payload, and launch sites

### 3. Interactive Visualizations
- **Folium Map** to visualize launch sites and proximity to railroads, highways, and coastlines
- **Plotly Dash App** with:
  - Launch Site dropdown to view success distribution
  - Payload slider to view correlation between mass and success

### 4. Predictive Modeling
- Trained and tuned several classification models:
  - Logistic Regression
  - Decision Tree
  - Support Vector Machine
  - K-Nearest Neighbors
- Used `GridSearchCV` for hyperparameter tuning
- Evaluated models using Jaccard Score, F1 Score, Accuracy, and Confusion Matrix

| Model               | Accuracy | F1 Score | Jaccard Score  |
|---------------------|----------|----------|----------------|
| Decision Tree       | 91.1%    | 0.94     | 0.88           |
| SVM                 | 87.7%    | 0.92     | 0.85           |
| Logistic Regression | 86.7%    | 0.91     | 0.83           |
| KNN                 | 85.5%    | 0.90     | 0.82           |

---

## Key Insights

- Heavier payloads (>6,000 kg) generally had lower success rates.
- Launch Site CCAFS LC-40 had the most failures.
- Booster version **FT** showed higher success consistency.
- The **Decision Tree Classifier** performed best with 91.1% accuracy.

---

## Final Presentation

The complete PowerPoint presentation of this project with all visualizations and insights can be found [here](https://github.com/user-attachments/files/21667267/Analyzing.and.Predicting.SpaceX.Launch.Outcomes.with.Data.pptx).

---

