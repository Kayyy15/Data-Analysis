# NHANES Body Measurement Data Analysis
[![Ask DeepWiki](https://devin.ai/assets/askdeepwiki.png)](https://deepwiki.com/Kayyy15/Data-Analysis)

This repository contains a comprehensive data analysis of the National Health and Nutrition Examination Survey (NHANES) 2017-2020 dataset. The project focuses on the body measurement data for adult males and females, exploring statistical properties, visualizing distributions, and analyzing the relationships between various anthropometric attributes.

## Key Analysis & Features

The analysis, conducted within the `nHaness data analysis.ipynb` notebook, includes the following key steps:
*   **Data Loading and Cleaning**: Ingesting the NHANES CSV data and handling commented header rows.
*   **Exploratory Data Analysis (EDA)**:
    *   Generating correlation matrices and visualizing them as heatmaps to understand attribute relationships.
    *   Plotting histograms to compare the weight distributions between males and females.
    *   Creating box-and-whisker plots to visualize differences in weight statistics and identify outliers across genders.
*   **Statistical Computation**: Calculating a full suite of descriptive statistics for male and female weights, including measures of location (mean, median), dispersion (standard deviation, variance, IQR), and shape (skewness, kurtosis).
*   **Feature Engineering**:
    *   Calculating Body Mass Index (BMI) and adding it as a new feature to the female dataset.
    *   Standardizing data using Z-scores for normalized comparison.
    *   Computing Waist-to-Height (WHtR) and Waist-to-Hip (WHR) ratios.
*   **Advanced Analysis**:
    *   Generating a pair plot matrix to visualize relationships between standardized variables (Weight, Height, Hip Circumference, Waist Circumference, and BMI).
    *   Calculating Pearson and Spearman correlation coefficients to quantify linear and monotonic relationships.
    *   Identifying individuals with the highest and lowest BMI values based on standardized scores.

## Dataset

The data is sourced from the US Centers for Disease Control and Prevention (CDC) National Health and Nutrition Examination Survey (NHANES), specifically from the 2017-March 2020 cycle. Two separate datasets are used:

*   `nhanes_adult_female_bmx_2020.csv`: Body measurements for 4,221 adult females (>= 18 years old).
*   `nhanes_adult_male_bmx_2020.csv`: Body measurements for 4,081 adult males (>= 18 years old).

Both datasets contain the following attributes:

| Column   | Description           | Unit |
|----------|-----------------------|------|
| `BMXWT`    | Weight                | kg   |
| `BMXHT`    | Standing Height       | cm   |
| `BMXARML`  | Upper Arm Length      | cm   |
| `BMXLEG`   | Upper Leg Length      | cm   |
| `BMXARMC`  | Arm Circumference     | cm   |
| `BMXHIP`   | Hip Circumference     | cm   |
| `BMXWAIST` | Waist Circumference   | cm   |

## Key Findings

*   **Weight Distribution**: Males generally have higher and more varied body weights than females. The male weight distribution is relatively symmetric, while the female distribution is right-skewed.
*   **Correlations**: There are strong positive correlations between weight and body circumferences (arm, waist, hip), as well as between weight and BMI. Height shows a weaker correlation with these metrics but is highly related to limb lengths.
*   **Health Ratios**: The Waist-to-Hip Ratio (WHR) is more tightly clustered for females. In contrast, males exhibit a wider WHR range and more outliers with high ratios.

## Getting Started

### Prerequisites
*   Python 3.x
*   Jupyter Notebook or JupyterLab

### Installation
1.  Clone this repository to your local machine:
    ```sh
    git clone https://github.com/kayyy15/data-analysis.git
    cd data-analysis
    ```
2.  Install the required Python packages:
    ```sh
    pip install -r requirements.txt
    ```

### Usage
To view and run the analysis, launch Jupyter Notebook/Lab and open the notebook file:
```
Notebooks/nHaness data analysis.ipynb
```
You can then execute the cells sequentially to reproduce the analysis.

## Libraries Used
*   **NumPy**: For numerical operations on arrays and matrices.
*   **Pandas**: For data manipulation and analysis, particularly for creating DataFrames for plotting.
*   **Matplotlib**: For creating static and interactive visualizations.
*   **Seaborn**: For high-level statistical data visualization.
*   **SciPy**: For scientific and technical computing, including statistical functions like `skew`, `kurtosis`, and correlation calculations.
