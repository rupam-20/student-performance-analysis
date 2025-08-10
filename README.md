# student-performance-analysis
Students Performance Dataset Analysis
📌 Overview
This project analyzes the StudentsPerformance dataset to explore the relationships between students' demographics, test preparation, and their scores in Math, Reading, and Writing.
The dataset is publicly available and contains performance records of high school students.

🎯 Project Goal
The main objective of this project is to:

Understand how demographic and educational factors influence student performance.

Identify patterns and correlations between different subject scores.

Provide visual insights that can help educators and policymakers improve academic outcomes.

📂 Dataset Description
File: StudentsPerformance (1).csv

Columns:
| Column Name                   | Description                                             |
| ----------------------------- | ------------------------------------------------------- |
| `gender`                      | Gender of the student (`male`/`female`)                 |
| `race/ethnicity`              | Ethnic group of the student                             |
| `parental level of education` | Highest education level achieved by the parents         |
| `lunch`                       | Type of lunch (`standard`/`free/reduced`)               |
| `test preparation course`     | Whether the student completed a test preparation course |
| `math score`                  | Score in mathematics (0–100)                            |
| `reading score`               | Score in reading (0–100)                                |
| `writing score`               | Score in writing (0–100)                                |


📊 Analysis Performed
Basic Data Exploration

Checked dataset structure, missing values, and data types.

Distribution Plots

Histograms and bar plots for each subject’s marks.

Scatter Matrix

Visualizing pairwise relationships between scores.

Correlation Matrix

Heatmap showing correlations between numeric features.
💡 Insights
Reading & Writing Scores: Strong positive correlation (students who perform well in one tend to perform well in the other).

Math vs Reading/Writing: Positive correlation but slightly weaker than reading-writing correlation.

Test Preparation Impact: Students who completed the preparation course tend to score higher.

Lunch Type Effect: Students with standard lunch generally perform better than those with free/reduced lunch.

🛠️ Requirements
Install dependencies:

pip install pandas matplotlib seaborn

▶️ How to Run
python
Copy code


import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
df = pd.read_csv("StudentsPerformance (1).csv")

# Correlation matrix
corr_matrix = df.corr(numeric_only=True)
sns.heatmap(corr_matrix, annot=True, cmap="coolwarm")
plt.show()

📈 Example Output
Correlation Matrix Heatmap: Shows strong positive correlation between reading and writing scores.

Distribution Graphs: Help understand the spread of marks.

Scatter Matrix: Highlights relationships between different subject scores.

📜 License
This dataset is used for educational and research purposes.


