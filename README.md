# Medical Data Visualizer

This project uses **Pandas**, **Matplotlib**, and **Seaborn** to perform exploratory data analysis and visualization on a dataset derived from medical examinations. It includes data cleaning, normalization, categorical visualization, and a heatmap of correlations.

## 📂 Dataset
The project uses a dataset of patient medical examination data stored in `medical_examination.csv`. The data includes values such as weight, height, cholesterol levels, glucose, and indicators like smoking and alcohol use.

---

## ✨ Features

### 🔹 Categorical Plot
Visualizes the counts of good (0) and bad (1) outcomes for:
- Cholesterol
- Glucose
- Smoking
- Alcohol intake
- Physical activity
- Overweight status  
Split by cardiovascular disease presence (`cardio=0` and `cardio=1`).

### 🔹 Heatmap
Displays the correlation matrix of numerical features after cleaning the dataset for outliers and logical inconsistencies.

---

## 📈 How It Works

### 1. Add a calculated `overweight` column:
Calculated using BMI > 25 → overweight = 1, else 0.

### 2. Normalize `cholesterol` and `gluc`:
- 1 → 0 (normal)
- >1 → 1 (bad)

### 3. Create Visualizations:
- `draw_cat_plot()`: Shows feature distributions by cardiovascular disease status.
- `draw_heat_map()`: Correlation matrix heatmap of medical metrics.

---

## 🧪 Sample Usage

```python
from medical_data_visualizer import draw_cat_plot, draw_heat_map

draw_cat_plot()
draw_heat_map()
🔍 Output
catplot.png

heatmap.png

🛠️ Requirements
Python 3

pandas

matplotlib

seaborn

bash
Copy
Edit
pip install pandas matplotlib seaborn
📊 Example Insights
Which health indicators are strongly correlated?

Are overweight or glucose levels predictive of cardiovascular issues?

How does activity or alcohol usage relate to health?

This project is ideal for practicing data cleaning, normalization, and matplotlib/seaborn visualizations with real-world health data.
