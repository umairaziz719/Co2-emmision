
# GDP Effect on CO2 Emission

This Python script analyzes the relationship between GDP and CO2 emissions (specifically from burning crop residues) using various data analysis and machine learning techniques. The code includes data preprocessing, data fitting, clustering, and forecasting models to explore and visualize trends in GDP and CO2 emissions over time for different countries.

## Features:
1. **Logistic Data Fitting**: The script fits GDP and CO2 emission data using a logistic curve to forecast future trends.
2. **Data Exploration**: Provides functionality to clean and extract relevant data for specific countries and indicators.
3. **Normalization**: Normalizes data to scale it between 0 and 1 for comparison and clustering.
4. **Clustering**: Uses K-means clustering to identify patterns and relationships between GDP and CO2 emissions across different countries.
5. **Correlation Heatmaps**: Visualizes the correlation between GDP and various CO2 emission sources.
6. **Forecasting**: Predicts future values of GDP and CO2 emissions up to the year 2050, including error ranges.

## Functions:
- **logistic(t, n0, g, t0)**: Computes the logistic function used for data fitting.
- **read_data(name)**: Reads a CSV file and returns both the original and transposed data.
- **data_exploration(data, country, series)**: Extracts the relevant data for a specific country and series.
- **norm(array)**: Normalizes an array to the range [0, 1].
- **data_fitting(data, country, indicator, col_name)**: Fits data using a logistic curve and plots it.
- **clustering_data(data, country, indicator, col_name, second_indicator, indicator_name)**: Applies K-means clustering to GDP and CO2 emission data and plots the results.
- **correlation_graph(data, country)**: Plots a heatmap of the correlation between GDP and CO2 emissions.
- **clustering_normalized_data(data, country, indicator, col_name, second_indicator, indicator_name)**: Applies K-means clustering on normalized data and visualizes the clusters.

## Usage:
1. Load the dataset by calling the `read_data` function with the path to the CSV file.
2. Use the `data_fitting` function to fit GDP and CO2 emission data for a given country.
3. Perform clustering analysis using the `clustering_data` function to examine the relationship between GDP and CO2 emissions.
4. Visualize correlation using `correlation_graph` to generate heatmaps for countries of interest.
5. Perform additional clustering analysis with normalized data using the `clustering_normalized_data` function.

## Requirements:
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- sklearn
- scipy

## Example:
```python
data, transpose_data = read_data("data.csv")
data_fitting(data, "Pakistan", "GDP (current US$)", "GDP")
data_fitting(data, "Pakistan", "Emission Totals - Emissions (CO2eq) (AR5) - Burning - Crop residues", "CO2 Burning - Crop residues")
clustering_data(data, "Pakistan", "GDP (current US$)", "GDP", "Emission Totals - Emissions (CO2eq) (AR5) - Crop Residues", "Crop Residues")
```

## Author:
Umair Aziz

---
