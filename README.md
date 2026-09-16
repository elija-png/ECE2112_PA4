# ECE-2112-PA4
**Made by: Elijah Theodore P. Rojo | 2ECE-D**

This repository contains the Programming Assignment 4 for our course "Advanced Computer Programming" for S.Y. 2026-2027. This project covers Pandas DataFrames filtering, conditional logic, aggregation, and data visualization using the `board2.xlsx` dataset.

---

## A. VISCOMM DATAFRAME

Load the `board2.xlsx` dataset into a Pandas DataFrame named `df` and compute the overall subject average across Math, GEAS, Electronics, and Communication. Create a filtered DataFrame named `VisComm` that contains only students whose Hometown is `'Visayas'` and whose Track is `'Communication'`.

The functions and methods used in this problem:
* **`pd.read_excel()`**: Reads an Excel spreadsheet into a Pandas DataFrame (`df`).
* **`.mean(axis=1)`**: Calculates the row-wise mean across selected subject columns (`Math`, `GEAS`, `Electronics`, `Communication`) to generate the `Average` column.
* **Bitwise AND Operator (`&`)**: Combines multiple conditions (`Hometown == 'Visayas'` and `Track == 'Communication'`) to form a boolean filter mask.
* **Column Indexing**: Extracts specified columns (`['Name', 'Gender', 'Math', 'Electronics', 'Average']`) for matching rows.
* **`len()`**: Computes the exact row count of the resulting filtered DataFrame.

---

## B. VISFEMALE DATAFRAME

Perform conditional indexing on `df` to create a new DataFrame named `VisFemale` containing female students hailing from Visayas.

The functions and methods used in this problem:
* **Bitwise AND Operator (`&`)**: Filters rows matching both conditions (`Hometown == 'Visayas'` and `Gender == 'Female'`).
* **Column Indexing**: Retains only the target columns (`['Name', 'Track', 'GEAS', 'Electronics', 'Average']`).
* **Data Inspection**: Displays the target subset DataFrame containing student scores and credentials.

---

## C. CATEGORY MEANS & PLOTTING

Analyze performance dynamics across categories by calculating mean `Average` scores grouped by Track, Gender, and Hometown, and visualize the results using Matplotlib.

The functions and methods used in this problem:
* **`.groupby()`**: Groups data by categorical variables (`Track`, `Gender`, and `Hometown`) to analyze summary metrics.
* **`.mean()`**: Computes the mean average score for each unique category group.
* **`plt.subplots()`**: Initializes a figure layout with multiple subplots sharing identical y-axis scales (`sharey=True`).
* **`.plot(kind='bar')`**: Renders bar charts comparing mean scores across categorical groups.
* **`.idxmax()` & `.max()`**: Identifies the specific category name and numeric value for the highest mean average score in each grouping.

---

Thank you for reading!  
To see the main Python notebook for Programming Assessment 4, click this link: https://github.com/elija-png/ECE2112_PA4/blob/main/PA4.ipynb

---
