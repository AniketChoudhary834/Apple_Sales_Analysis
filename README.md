# Apple Product Sales Insights

This Jupyter Notebook provides an analysis of a dataset related to Apple products. It includes various steps for data loading, preprocessing, visualization, and identification of the top 10 smartphones. The notebook is organized into several sections to guide the user through the process.

## Table of Contents

1. [Introduction](#Introduction)
2. [Data Loading](#Data-Loading)
3. [Data Preprocessing](#Data-Preprocessing)
4. [Data Visualization](#Data-Visualization)
5. [Top 10 Smartphones](#Top-10-Smartphones)
6. [Conclusion](#Conclusion)

## Introduction

This section provides an overview of the notebook's purpose, which is to analyze a dataset containing information about Apple products. The analysis includes loading the data, cleaning it, visualizing various aspects, and identifying the top 10 smartphones based on specific criteria.

## Data Loading

In this section, the notebook loads the dataset using `pandas`. The data is read from a CSV file and displayed to give an initial understanding of its structure.

```python
import pandas as pd

data = pd.read_csv('apple_data.csv')
data.head()
```

## Data Preprocessing

This section covers the preprocessing steps required to clean and prepare the data for analysis. It includes handling missing values, converting data types, and performing any necessary transformations.

```python
# Example preprocessing step
data.dropna(inplace=True)
```

## Data Visualization

Here, various visualizations are created to explore and understand the data better. The visualizations include scatter plots, bar charts, and histograms using libraries like `matplotlib` and `plotly`.

```python
import plotly.express as px

fig = px.scatter(data, x='Number Of Ratings', y='Discount Percentage')
fig.show()
```

## Top 10 Smartphones

This section identifies the top 10 smartphones based on specific criteria such as ratings, reviews, or other relevant metrics. The criteria and methodology for selecting the top 10 smartphones are explained here.

```python
# Example code to find the top 10 smartphones
top_10_smartphones = data.sort_values(by='Number Of Ratings', ascending=False).head(10)
top_10_smartphones
```

## Conclusion

The conclusion summarizes the key findings from the analysis and provides insights derived from the visualizations and the identification of the top 10 smartphones.

## Usage

1. **Requirements**: Make sure you have the necessary Python libraries installed. You can install them using:
   ```bash
   pip install pandas plotly
   ```

2. **Running the Notebook**: Open the Jupyter Notebook in your preferred environment (e.g., Jupyter Lab, Jupyter Notebook) and run the cells sequentially to reproduce the analysis.

3. **Modifying the Analysis**: You can modify the code to suit your needs. For instance, you can change the file path for the dataset, adjust the preprocessing steps, or create additional visualizations.

## Author

This notebook was created by Aniket Choudhary.
