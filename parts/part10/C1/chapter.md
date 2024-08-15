# Estimating Air Pollution in Colombia


<h2> Air Quality: Explore Phase </h2>

<div class="ui red segment">
  <a class="ui red ribbon label">Data Loading and Initial Exploration</a>

  **Objective:** Load air quality data into the environment and perform an initial exploration to understand the dataset's structure and contents.

  **Tasks:**
  - **Load the dataset** using `pandas` and display the first few rows to get an overview.
  - **Check for missing values** across the dataset using `.isnull().sum()` to identify columns with incomplete data.
  - **Explore basic statistics** of the dataset with `.describe()` to understand the distribution of data.
</div>

<div class="ui orange segment">
  <a class="ui orange ribbon label">Data Cleaning and Preprocessing</a>

  **Objective:** Prepare the dataset for deeper analysis by addressing missing data and ensuring consistency.

  **Tasks:**
  - **Calculate the total number of records and the percentage of missing values** in each column to assess the extent of missing data.
  - **Drop or impute missing values** based on the calculated percentages to ensure the dataset is suitable for analysis.
  - **Standardize data formats** and correct any inconsistencies in the dataset.
</div>

<div class="ui yellow segment">
  <a class="ui yellow ribbon label">Exploratory Data Analysis (EDA)</a>

  **Objective:** Gain insights into the data by visualizing key features and identifying trends, patterns, and anomalies.

  **Tasks:**
  - **Visualize key features** such as pollutant levels over time using time series plots.
  - **Examine the distribution** of pollutants and other variables to identify outliers or unusual trends.
  - **Analyze relationships** between different variables to understand correlations or dependencies.
</div>

<div class="ui blue segment">
  <a class="ui blue ribbon label">Feature Engineering</a>

  **Objective:** Enhance the dataset with new features that can improve the analysis or model performance.

  **Tasks:**
  - **Create new features** based on existing data, such as aggregating pollutant levels over different time windows.
  - **Transform variables** if necessary to meet the assumptions of modeling techniques or to highlight important patterns.
  - **Handle categorical variables** by encoding them into numerical formats suitable for analysis.
</div>

<div class="ui purple segment">
  <a class="ui purple ribbon label">Modeling Preparation</a>

  **Objective:** Prepare the dataset for machine learning modeling by selecting relevant features and splitting the data.

  **Tasks:**
  - **Select features** that are most relevant to the prediction task, based on the exploratory analysis.
  - **Split the dataset** into training and testing sets to evaluate model performance.
  - **Normalize or scale data** to ensure that models can learn effectively from the dataset.
</div>

<div class="ui pink segment">
  <a class="ui pink ribbon label">Modeling and Evaluation</a>

  **Objective:** Develop and evaluate predictive models for air quality forecasting.

  **Tasks:**
  - **Train models** using the prepared dataset and evaluate their performance using appropriate metrics.
  - **Compare different models** to determine which performs best on the task at hand.
  - **Tune hyperparameters** to improve model performance where necessary.
</div>

<div class="ui brown segment">
  <a class="ui brown ribbon label">Results Visualization and Interpretation</a>

  **Objective:** Visualize the results of the modeling and provide interpretations of the findings.

  **Tasks:**
  - **Plot predictions** against actual values to assess the accuracy of the models.
  - **Visualize model performance metrics** such as error distributions and comparison charts.
  - **Interpret results** in the context of air quality forecasting, discussing the implications and potential applications.
</div>














<br> <br> <br> <br>


























<h2> Air Quality: Design Phase </h2>

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
