# Missing Data



## Problem Overview

<div style="display: flex; justify-content: space-around;">
  <figure style="margin-right: 20px;">
    <img src="../../../_images/MissingDataAirQualityUseCase.png" alt="Missing Data Air Quality UseCase" width="300"/>
    <figcaption style="text-align: center;">Map of Bogotá displaying air quality sensor readings, highlighting the unequal distribution of sensors across the city and the presence of gaps in data collection, which underscore the challenges of data inequality and missing information in AI-based environmental monitoring systems.</figcaption>
  </figure>
  <figure>
    <img src="../../../_images/PartialDataAirQualityUseCase.png" alt="Partial Data Air Quality UseCase" width="300"/>
    <figcaption style="text-align: center;">Map highlighting areas of Bogotá where air quality data is only partially available. The presence of partial data can significantly impact the effectiveness of AI models, leading to challenges in accurately predicting and managing air quality, especially in under-monitored regions.</figcaption>
  </figure>
</div>



- **Importance of Sensor Data in AI**: Sensor data is essential for AI applications, providing the raw input for environmental monitoring and public health management.

- **Data Inequality in Sensor Distribution**: Unequal placement of sensors, often concentrated in more affluent areas, leads to gaps in data coverage and reflects broader societal inequalities.

- **Impact on Underserved Communities**: Areas with fewer sensors, typically less affluent, may lack critical data, putting residents at greater risk of health issues due to unmonitored air quality.

- **Challenges of Missing Data**: Missing data from sensors due to malfunctions or maintenance can undermine the accuracy and reliability of AI models.

- **Techniques to Handle Missing Data**: AI systems can use methods like data imputation or robust modeling to manage and mitigate the effects of missing data.

- **Need for Equitable AI Implementation**: To ensure AI benefits all segments of society, data collection must be equitable, and AI models must be designed to handle data gaps effectively.

- **Social Responsibility in AI**: Addressing data inequality and missing data in AI systems is crucial for building socially responsible and reliable AI solutions that serve the public good.




## K-Nearest Neighbor (KNN) for Imputing Missing Data


One effective method for imputing missing data in air quality datasets is the K-Nearest Neighbor (KNN) algorithm. KNN is a non-parametric, instance-based learning method that uses the characteristics of the nearest data points to estimate the missing values. The principle behind KNN is that data points that are close to each other in the feature space (i.e., similar in terms of the observed variables) are likely to have similar values for the missing attribute.




### Variations of K-Nearest Neighbor for Imputation

Several variations of the KNN algorithm have been developed to handle missing data more effectively, each with its own strengths and limitations. Below are the most commonly used variations:

1. **Basic K-Nearest Neighbor (KNN):**
   - **Description:** The simplest form of KNN where the missing value is imputed by averaging the values of the 'k' nearest neighbors.
   - **Pros:** Easy to implement and understand; performs well with small datasets and when the data is not highly skewed.
   - **Cons:** Sensitive to the choice of 'k'; may not work well with high-dimensional data or when the dataset contains noise.

2. **Weighted K-Nearest Neighbor (WKNN):**
   - **Description:** In this variation, the influence of each neighbor on the imputed value is weighted by the inverse of its distance to the missing data point. Closer neighbors have more influence on the imputation.
   - **Pros:** More accurate than basic KNN as it accounts for the varying significance of neighbors; reduces the impact of distant, potentially less relevant neighbors.
   - **Cons:** Computationally more expensive; sensitive to the choice of distance metric and the weighting function.

3. **Distance-Weighted KNN with Correlation Adjustment:**
   - **Description:** Extends the WKNN by adjusting weights based on the correlation between variables. Highly correlated variables are given more weight during imputation.
   - **Pros:** Effective in datasets where certain variables are highly correlated, improving the accuracy of imputation.
   - **Cons:** Requires computation of correlation matrices, adding to complexity; may not perform well if the correlation structure of the data is weak.

4. **Iterative KNN Imputation:**
   - **Description:** An iterative approach where KNN is applied multiple times. In each iteration, previously imputed values are refined by considering the updated dataset.
   - **Pros:** Can lead to more accurate imputations as it refines estimates with each iteration; handles large amounts of missing data better.
   - **Cons:** Time-consuming and computationally intensive; risk of overfitting if the number of iterations is too high.

5. **KNN with Multiple Imputation (KNN-MI):**
   - **Description:** Combines KNN with a multiple imputation approach where several imputations are performed to capture the uncertainty of missing data. The final imputed value is an average or weighted combination of these imputations.
   - **Pros:** Provides a measure of uncertainty in the imputation; reduces bias in statistical analysis by considering multiple plausible values.
   - **Cons:** Complex and resource-intensive; requires careful tuning and consideration of the number of imputations.

### Pros and Cons for KNN Variations

| **KNN Variation**                      | **Pros**                                                                 | **Cons**                                                      |
|----------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------|
| **Basic KNN**                          | Easy to implement, intuitive, works well with small datasets             | Sensitive to 'k', struggles with high-dimensional/noisy data   |
| **Weighted KNN (WKNN)**                | More accurate by considering distance; reduces impact of distant neighbors | Higher computational cost, sensitive to distance metric       |
| **Distance-Weighted KNN with Correlation Adjustment** | Improves accuracy by leveraging correlations between variables | Complex, requires computation of correlation matrices          |
| **Iterative KNN Imputation**           | Refines imputations through iterations, handles large missing data better | Time-consuming, risk of overfitting                           |
| **KNN with Multiple Imputation (KNN-MI)** | Captures uncertainty, reduces bias in analysis                              | Complex, resource-intensive, requires tuning                   |




