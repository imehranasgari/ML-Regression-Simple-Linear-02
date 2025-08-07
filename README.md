
# 🧾 Linear Regression (Tips)

## 🎯 Problem Statement
This notebook tackles a regression problem: predicting the **tip amount** based on features like `total_bill`, `size`, `day`, and others from the `tips` dataset.  
The objective is to explore how linear relationships can be modeled to understand consumer behavior in tipping.

## 📝 Note
The purpose of this project is not just achieving high accuracy, but clearly **demonstrating the machine learning workflow**—from exploration and preprocessing to modeling and evaluation.  
هدف اصلی این پروژه نشون دادن روند اجرای مدل رگرسیون خطی هست؛ تمرکز بر فهم ساختار کاره نه صرفاً رسیدن به کمترین خطا.

---

## ⚙️ Solution Approach

### 1. Exploratory Data Analysis (EDA)
- Load `tips` dataset from Seaborn.
- View dataset shape, sample rows, and summary statistics.
- Analyze tip behavior by `day`, `smoker`, and `size`.
- Visualize patterns using Seaborn's `catplot`.

### 2. Data Preprocessing
- Convert categorical columns:
  - `sex`: 'Male' → 0, 'Female' → 1
  - `smoker`: 'No' → 0, 'Yes' → 1
- One-hot encode `day` and `time`, merge to original dataframe.

### 3. Model Building & Evaluation
- Define features `X = [total_bill, size]`, target `Y = tip`.
- Split data into train/test sets (`random_state=26`).
- Train `LinearRegression` model.
- Predict on test set and visualize residuals.
- Evaluate with:
  - **MAE** (Mean Absolute Error)
  - **MSE** (Mean Squared Error)
  - **RMSE** (Root Mean Squared Error)

### 4. Prediction on New Input
- Predict tip for new customer (`total_bill=16.99`, `size=2`).
- Print model coefficients and intercept.

---

## 🧰 Technologies & Libraries
- **Python 3**
- **NumPy** – numerical operations  
- **Pandas** – data manipulation  
- **Matplotlib** & **Seaborn** – data visualization  
- **Scikit-learn** – regression modeling & evaluation

---

## 💻 Installation & Execution Guide

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
jupyter notebook Linear_Regression_Tips.ipynb
````

Make sure to run the notebook in an environment with Jupyter or JupyterLab installed.

---

## 📊 Key Results / Performance

| Metric   | Value  |
| -------- | ------ |
| **MAE**  | 0.7719 |
| **MSE**  | 1.2208 |
| **RMSE** | 1.1049 |

* **Coefficients**:
  `total_bill`: 0.1213, `size`: -0.0162
* **Intercept**: 0.7502
* **Prediction for total\_bill=16.99 & size=2** → Tip ≈ **2.78**

---

## 🖼️ Sample Outputs

| Sample Data        |
| ------------------ |
| `df.head()` shows: |

```text
   total_bill   tip     sex smoker  day    time  size
0       16.99  1.01  Female     No  Sun  Dinner     2
1       10.34  1.66    Male     No  Sun  Dinner     3
...
```

* **Day Count Plot**
  ![Day Count](images/day_count_plot.png)

* **Day vs. Size Plot**
  ![Day Size Count](images/day_size_count_plot.png)

* **Correlation Heatmap**
  ![Correlation Heatmap](images/correlation_heatmap.png)

* **Residuals Histogram**
  ![Residuals](images/residuals_histogram.png)

---

## ✨ What This Project Demonstrates
* Proficiency in data analysis and visual interpretation of relationships
* Strong understanding of data preprocessing and encoding categorical variables
* Familiarity with model evaluation using common metrics (MAE, MSE, RMSE)
* Structured practice to deepen practical understanding of linear regression
* Effective use of data visualization to better understand data behavior

---

## 👨‍💻 Author

**Mehran Asgari**
📧 [imehranasgari@gmail.com](mailto:imehranasgari@gmail.com)
🔗 [github.com/imehranasgari](https://github.com/imehranasgari)

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

```

