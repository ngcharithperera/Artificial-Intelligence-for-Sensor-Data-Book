# Estimating Air Pollution in Colombia


<h2>Air Quality: Design Phase</h2>

<div class="ui red segment">
  <a class="ui red ribbon label">Data Loading and Preprocessing</a>

  **Objective:** Load air quality data and preprocess it to make it suitable for analysis.

  **Tasks:**
  - **Read raw data** from files (e.g., CSV).
  - **Correct date formats** and handle missing values using functions like `fix_dates`.
  - **Parse and standardize coordinate data** if needed (e.g., converting DMS to decimal).
  - Ensure that the data is **clean and consistent** for further analysis.
</div>

<div class="ui orange segment">
  <a class="ui orange ribbon label">Exploratory Data Analysis (EDA)</a>

  **Objective:** Understand the distribution, trends, and anomalies in the air quality data.

  **Tasks:**
  - **Visualize time series** of various pollutants (e.g., PM2.5, NO2) across different stations.
  - Identify **patterns, peaks, and trends** over time.
  - **Analyze the distribution and frequency** of missing data.
</div>

<div class="ui yellow segment">
  <a class="ui yellow ribbon label">Handling Missing Data</a>

  **Objective:** Develop and apply strategies to impute or fill in missing data, which is common in environmental datasets.

  **Tasks:**
  - **Visualize the distribution of gaps** in the data to understand the extent and nature of missingness.
  - Apply various **imputation techniques**:
    - **K-Nearest Neighbors (KNN):** For imputing missing values based on the nearest neighbors in time or space.
    - **Linear Interpolation:** For estimating missing values by interpolating between existing data points.
    - **Neural Networks:** For more sophisticated imputation by predicting missing values using a trained model.
</div>

<div class="ui blue segment">
  <a class="ui blue ribbon label">Modeling and Prediction</a>

  **Objective:** Build and evaluate models to predict air pollutant concentrations, potentially filling in gaps or forecasting future values.

  **Tasks:**
  - **Train machine learning models**, particularly neural networks, to predict pollutant concentrations based on features such as time, location, and nearby pollutant levels.
  - **Evaluate model performance** using metrics like Mean Absolute Error (MAE).
  - **Visualize predictions** against actual data to assess accuracy.
</div>

<div class="ui purple segment">
  <a class="ui purple ribbon label">Interactive Data Exploration</a>

  **Objective:** Allow users to interactively explore the data and model predictions.

  **Tasks:**
  - Use **ipywidgets** to create interactive plots where users can select different stations, pollutants, and time ranges.
  - Facilitate exploration of the effects of different **imputation methods** and visualize the results.
</div>

<div class="ui pink segment">
  <a class="ui pink ribbon label">Imputation of Non-Target and Target Pollutants</a>

  **Objective:** Impute missing data specifically for non-target pollutants first and then for target pollutants like PM2.5.

  **Tasks:**
  - Use **linear interpolation** to impute non-target pollutants.
  - Apply **neural network models** to impute missing values for target pollutants, ensuring that the imputed data is accurate and reliable.
</div>

<div class="ui brown segment">
  <a class="ui brown ribbon label">Visualization and Reporting</a>

  **Objective:** Create clear visualizations that communicate the findings and effectiveness of different methods.

  **Tasks:**
  - **Plot the imputed data** alongside real data to show the effectiveness of the imputation methods.
  - Generate **summary plots** that highlight the distribution of gaps, the performance of models, and the accuracy of predictions.
</div>
