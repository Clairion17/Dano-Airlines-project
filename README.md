# Dano-Airlines-project
Dano Airlines recently recorded its lowest-ever passenger satisfaction score — below 50%. As a Data Analyst,i will analyze the passenger survey data, uncover the root causes of dissatisfaction, and provide clear, actionable recommendations to help leadership take immediate steps toward improvement.
🎯 Objectives

Analyze survey data to determine the main drivers of low satisfaction

Identify strengths and weaknesses across service categories

Provide data-driven insights and recommendations

Build visuals that help leadership quickly understand key issues

🧰 Tech Stack
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Jupyter Notebook
- Power BI / Tableau (optional for dashboards)
- CSV dataset (Passenger Survey Data)

📂 Project StructureDano-Airlines-Analysis/
│
├── data/
│   ├── passenger_survey.csv
│
├── notebooks/
│   ├── dano_airlines_analysis.ipynb
│
├── visuals/
│   ├── satisfaction_scores.png
│   ├── correlation_heatmap.png
│
├── README.md
└── requirements.txt

📝 Sample Data Loading & Cleaning Code
import pandas as pd

# Load dataset
df = pd.read_csv("data/passenger_survey.csv")

# Quick look at data
print(df.head())
print(df.info())

# Handle missing values
df.fillna(df.mean(numeric_only=True), inplace=True)

# Convert categorical data
categorical_cols = df.select_dtypes(include="object").columns
df[categorical_cols] = df[categorical_cols].astype("category")


📉 Exploratory Data Analysis (EDA)
import matplotlib.pyplot as plt

plt.figure(figsize=(8,5))
df['Satisfaction'].value_counts().plot(kind='bar')
plt.title('Passenger Satisfaction Distribution')
plt.xlabel('Satisfaction Level')
plt.ylabel('Count')
plt.show()

Correlation Heatmap
import seaborn as sns

plt.figure(figsize=(10,8))
sns.heatmap(df.corr(), annot=True, fmt=".2f", cmap="Blues")
plt.title('Feature Correlation Heatmap')
plt.show()

🔍 Key Questions Answered

✔ What categories contributed most to the low satisfaction score?
✔ Which touchpoints—Check-in, In-flight service, Baggage, Delays—require urgent attention?
✔ What patterns exist across age groups, travel class, and flight routes?
✔ What actions can Dano Airlines take to improve satisfaction quickly?

📌 Sample Findings (Replace with Your Insights)
- In-flight service and baggage handling scored lowest across all passengers.
- Business class passengers reported higher satisfaction than economy.
- Long-haul flights experienced the highest volume of complaints.
- Younger passengers (18–30) scored lowest overall satisfaction.

- 📈 Dashboard (Optional Power BI/Tableau)

Overall Satisfaction Score

Top 5 Low-Scoring Survey Items

Customer Segment Analysis

Delay Impact Analysis

🛠 Recommendations
- Improve baggage handling processes to reduce loss/damage incidents.
- Retrain cabin crew to enhance in-flight service quality.
- Address recurring long-haul delays through scheduling optimization.
- Introduce incentives such as vouchers for affected passengers.

📦 Installation
pip install -r requirements.txt

🧪 Run the Analysis
jupyter notebook notebooks/dano_airlines_analysis.ipynb

👤 Author

Amara Anagbor
Data Analyst | Dano Airlines Project
