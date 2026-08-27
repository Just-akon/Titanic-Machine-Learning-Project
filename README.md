# Titanic-Machine-Learning-Project
A beginner data science project analyzing Titanic passenger data and using Logistic Regression to predict survival.
# Titanic Survival Prediction

A beginner data science project exploring which passenger variables had the most influence on survival aboard the Titanic and using logistic regression to predict survival.

## 1. Problem Statement

The main question I focused on was: **What variable had the most say in passenger survival?**

Understanding the factors associated with survival can help demonstrate how data analysis and machine learning can be used to identify patterns in historical data and make predictions from those patterns.

## 2. Dataset

The dataset contains **891 Titanic passenger records**.

**Source:** https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv

Key columns used in the analysis included:

* `Survived` — whether the passenger survived
* `Pclass` — passenger class
* `Sex` — passenger gender
* `Age` — passenger age
* `SibSp` — number of siblings/spouses aboard
* `Parch` — number of parents/children aboard
* `Fare` — passenger fare
* `Embarked` — port where the passenger boarded

## 3. My Approach

### Data Cleaning

I handled missing data by:

* Replacing missing values in the `Age` column with the **median age**.
* Filling missing values in the `Embarked` column with **"Un"**.
* Leaving out `Cabin` because it was not relevant to my analysis.

I also dropped the `Name`, `PassengerId`, `Ticket`, and `Cabin` columns because they did not prove to be relevant to passenger survival for this project.

### Exploratory Data Analysis

I used **Pandas, NumPy, Matplotlib, and Seaborn** to explore the dataset and look for patterns.

The visualizations I created included:

* **Pie chart** — showed the gender distribution of passengers.
* **Bar chart** — compared the number of casualties with the number of survivors.
* **Histograms** — showed the distribution of passengers by age and fare.
* **Bar chart** — compared where passengers boarded from.
* **Scatter plot** — showed the negative correlation between `Fare` and `Pclass`.

### Modeling

After exploring and preparing the data, I trained a **Logistic Regression** model using scikit-learn to predict whether a passenger survived.

## 4. Key Findings

One of the most interesting findings was that the data alone could not show **when more men died or why more women survived**. This may have been influenced by factors or information that were not included in the dataset, so the available data was not enough to explain the reason behind this pattern.

The scatter plot also showed a **negative correlation between Fare and Pclass**.

## 5. Model Results

The Logistic Regression model achieved an accuracy of **80.9%**.

The confusion matrix was:

```text
[[97 13]
 [21 47]]
```

In plain language, the model correctly classified **97 passengers who did not survive** and **47 passengers who survived**. It incorrectly classified **13 passengers who did not survive** and **21 passengers who survived**.

An accuracy of 80.9% means that the model correctly predicted the survival outcome for roughly **8 out of every 10 passengers** in the evaluated data.

## 6. How to Run This Project

To run this project, open the Jupyter Notebook containing the analysis and make sure Python is installed.

The main libraries required are:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* scikit-learn

The dataset can be loaded from the provided Titanic CSV source, after which the notebook can be run through the data-cleaning, exploratory analysis, visualization, and modeling steps.

## 7. What I'd Do Next

If I continued this project, **I would add more features** to the analysis and model to see whether additional information could improve the predictions and provide more insight into the factors associated with survival.
