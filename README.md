# timeseries-anomaly-detection

## Overview
This repository demonstrates time series anomaly detection using the Isolation Forest algorithm, with a focus on how sliding window features can improve detection accuracy. The main workflow is implemented in the provided Jupyter notebook.

## What is Done in the Notebook

1. **Data Loading and Preparation**
   - Loads a CPU utilization time series dataset (`ec2_cpu_utilization.csv`).
   - Parses timestamps and marks known anomalies for evaluation.

2. **Visualization**
   - Plots the raw time series data, highlighting known anomalies for visual inspection.

3. **Anomaly Detection with Isolation Forest (Raw Values)**
   - Trains an Isolation Forest model using only the raw value at each time point.
   - Evaluates performance using a confusion matrix, showing the model's ability to distinguish normal points from anomalies.

4. **Anomaly Detection with Sliding Window Features**
   - Constructs sliding window features, where each sample is a short sequence of recent values.
   - Handles missing values in the window using imputation.
   - Trains a new Isolation Forest model on these windowed features.
   - Evaluates performance with a confusion matrix, comparing results to the raw value approach.

5. **Summary and Insights**
   - Compares the two approaches, showing that the sliding window method reduces false positives and improves anomaly detection.
   - Concludes that transforming time series into short sequences helps the model capture local patterns and improves accuracy.

## How to Use
1. Open `notebook.ipynb` in Jupyter Lab or Notebook.
2. Run the cells sequentially to reproduce the analysis and visualizations.
3. Review the summary for key findings.

## Requirements
- Python 3.8+
- pandas, numpy, matplotlib, scikit-learn
