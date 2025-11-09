# MSCS_634_Lab_2

# KNN and RNN Classifier Performance Analysis - Wine Dataset

## Purpose of the Lab Work

In this lab, we explore the performance of two machine learning classifiers, K-Nearest Neighbors (KNN) and Radius Neighbors (RNN), using the Wine Dataset from the `sklearn` Python library. The primary objective is to analyze the impact of different parameter values on model accuracy and to visualize key results. By applying KNN and RNN models, we aim to understand how parameter choices influence classification performance and determine which classifier might be preferable for different types of data distributions.

## Key Insights from Clustering Results and Observations

- **KNN (K-Nearest Neighbors)**: The best performance was achieved with a `k` value of 15, resulting in an accuracy of 97.22%. This suggests that for this dataset, the number of neighbors plays a significant role in the model's ability to make accurate predictions. A moderate value of `k` helps in preventing overfitting or underfitting.
  
- **RNN (Radius Neighbors)**: The best radius value of 350 resulted in a relatively low accuracy of 38.89%. This indicates that RNN may not perform as well on this dataset, possibly due to the dataset's inherent structure, where a fixed number of neighbors (as used in KNN) might be more suitable than a fixed radius distance.

- **Overall Comparison**: KNN outperforms RNN in this case, especially with moderate values of `k`. KNN is likely more effective for datasets with clear, separable clusters, whereas RNN may be more appropriate for datasets with irregular or non-linear decision boundaries.

## Challenges Faced and Decisions Made

1. **Parameter Selection**: A key challenge was choosing appropriate values for `k` in KNN and the `radius` in RNN. After testing multiple values, we found that a `k` value of 15 gave the best performance for KNN, while a radius value of 350 worked best for RNN.

2. **Model Comparison**: The challenge of comparing KNN and RNN arose because the performance of RNN was relatively poor compared to KNN, likely due to the nature of the Wine dataset, which may not require a radius-based classification technique.

3. **Data Scaling**: Since KNN and RNN are sensitive to the scale of the data, we applied standardization to the dataset using `StandardScaler` to ensure that all features contributed equally to the distance calculations.

## Conclusion

This lab provided valuable insights into how classifier parameters influence performance. KNN performed better on the Wine dataset, while RNN may be more suited to datasets with complex decision boundaries. Future work could involve experimenting with different parameter ranges or exploring other classification models for better performance.
