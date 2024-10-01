
# Data Description  
Contains more than 10,000 records of restaurants' in Sydney in the year 2018. 
| Column          | Description                                                  | Example                                      |
|-----------------|--------------------------------------------------------------|----------------------------------------------|
| 'address'       | Restaurant's address (text)                                  | 371A Pitt Street, CBD, Sydney                |
| 'cost'          | Average cost for two people in AUD (numeric)                | 50.0                                         |
| 'cuisine'       | Cuisines served by the restaurant (list)                    | [Thai, Salad]                                |
| 'lat'           | Latitude (numeric)                                          | -33.876059                                   |
| 'link'          | URL (text)                                                  | [https://www.zomato.com/sydney/sydney-madang-cbd](https://www.zomato.com/sydney/sydney-madang-cbd) |
| 'lng'           | Longitude (numeric)                                         | 151.207605                                   |
| 'phone'         | Phone number (numeric)                                      | 02 8318 0406                                |
| 'rating_number' | Restaurant rating (numeric)                                 | 4.0                                          |
| 'rating_text'   | Restaurant rating (text)                                    | Very Good                                    |
| 'subzone'       | Suburb in which the restaurant resides (text)               | CBD                                          |
| 'title'         | Restaurant's name (text)                                    | Sydney Madang                                |
| 'type'          | Business type (list)                                        | [Casual Dining]                              |
| 'votes'         | Number of users who provided the rating (numeric)           | 1311.0                                       |
| 'groupon'       | Is the restaurant promoting itself on Groupon.com? (boolean) | False                                        |

## Features

### Part A (dsts_a1)
- Focuses on exploratory analysis of categorical and numerical variables:
  - Analyzes the quantity of different culinary offerings in restaurants located in Sydney.
  - Includes a pricing/cost analysis supporting the statement: "Restaurants with excellent ratings tend to be very expensive, while those with poor ratings are rarely costly."
  - Various visual aids, such as histograms, bar charts, and box plots, were used to explore the dataset's variables.

### Part B (dsts_geopandas)
- Emphasizes data visualization, particularly the concentration of restaurants in specific suburbs based on a culinary theme:
  - Utilizes a 'sydney.geojson' file to merge additional attributes like SSC_CODE (State Suburbs Code) and geometric polygonal information into the original dataset.
  - Matplotlib was used to generate a heatmap illustrating the distribution of restaurants in a specific suburb, visualized by cuisine type.

![download](https://github.com/user-attachments/assets/b54d8931-d015-4dae-94cf-09e30e8f5b5b)

## Extra Map (Folium)

![image](https://github.com/user-attachments/assets/eb0c2c2a-e78c-43cb-b53d-612b19003e5e)

### Part C: Regression and Classification Models

- **Regression Models**:
  - **Model 1** (Mean Squared Error: 0.14493985134981474, R-squared: 0.2643760108454495).
  - **Model 2** (Gradient Descent with standardized values):
    - Mean Squared Error: 0.16264968064453356
    - R-squared: 0.17449199929375825

- **Classification Models**:
  - A **binary classification model** using logistic regression to classify restaurants as either:
    - (Poor, Average) = 1
    - (Good, Very Good, Excellent) = 2.
  
  **Logistic Regression Model Performance**:
  - Accuracy: 0.9603
  - Precision: 0.9606
  - Recall: 0.9799
  - F1 Score: 0.9701
  - ROC AUC Score: 0.9513
  - Confusion Matrix:
    - [[926, 19], [38, 454]]

- **Additional Classification Models**:
  - **Support Vector Machine (SVM)** with Linear and Radial Basis Function (RBF) kernels, **Decision Tree**, and **Random Forest** models were also applied. The performance metrics for these models are as follows:

| Model            | Accuracy | Precision | Recall   | F1 Score | ROC AUC |
|------------------|----------|-----------|----------|----------|---------|
| Linear SVM       | 1.000000 | 0.960581  | 0.979894 | 0.970141 | 0.951329|
| RBF SVM          | 0.856646 | 0.960581  | 0.979894 | 0.970141 | 0.951329|
| Decision Tree    | 1.000000 | 0.960581  | 0.979894 | 0.970141 | 0.951329|
| Random Forest    | 1.000000 | 0.960581  | 0.979894 | 0.970141 | 0.951329|

# Tableau Dashboard for the dataset :  
[Tableau](https://public.tableau.com/app/profile/hardik.agarwal8035/viz/Hardik_Agarwal_Assignment1/Dashboard1)

