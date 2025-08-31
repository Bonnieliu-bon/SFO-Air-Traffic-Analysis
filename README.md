# SFO-Air-Traffic-Analysis
This repository is a complete data science case study in applying a full-stack analytics approach, from Exploratory Data Analysis to a sophisticated combined K-means clustering &amp; Random Forest machine learning model to predict passenger traffic with precision. It transforms raw data into a strategic playbook for enhancing operations and marketing.

## Project Summary

This project, titled "Optimizing Operations and Strategy at San Francisco International Airport (SFO)," is a comprehensive data analysis of SFO's air traffic passenger data. The main goal is to provide a hypothetical airline with a data-driven strategy to gain a competitive edge in the SFO market. The analysis progresses from foundational Exploratory Data Analysis (EDA) to a sophisticated combined machine learning model, and finally to a business-focused interpretation of the findings. Key methods include K-means clustering for passenger segmentation, a Random Forest regressor for traffic prediction, and time-series decomposition for understanding seasonal trends. The project's output is a set of actionable recommendations for route planning, marketing, and operational efficiency, all framed within a Tableau storyboard for clear communication.

## Key Questions

This project answers several key questions across different stages of the analysis:

- **Which airline has the most exposure in SFO airport?** *The EDA process can identify the airlines with the highest total passenger count, indicating their market share at SFO.*

- **Which terminal handles more domestic or international traffic in SFO airport?** *By analyzing passenger count by Terminal and Flight Type, the project can reveal which terminals are hubs for specific types of flights.*

- **Which region contributes the most passengers seasonally in SFO airport?** *The time-series analysis for the top GEO Region (United States) reveals a strong seasonal pattern, with predictable peaks and troughs in passenger traffic.*

- **Can we predict passenger count using airline, region, and month?** *Yes, the Random Forest model confirms that Month and GEO Region are important predictors. The most significant finding, however, is that adding the Cluster feature—derived from a prior K-means analysis—improves the prediction accuracy, proving that segmenting the data first is a superior approach.*

## Folder Structure

The repository is organized into a clear, logical folder structure to ensure maintainability and ease of use.

- 01 project_management/: Contains project planning documents, meeting notes, and the initial business case outline.

- 02 data/: Stores the raw dataset (Air_Traffic_Pax_v3.csv) and any processed data (Air_Traffic_Prepared_Data.csv) ready for visualization.

- 03 scripts/: Contains all the Python scripts used for data cleaning, analysis, and model building, including the step-by-step preparation code.

- 04 analysis/: Holds the outputs of the analysis, such as the Tableau storyboard file, and images of the generated charts.

- 05 sent_to_client/: A folder for final deliverables, including the Tableau storyboard package and a summary report.

## Code Overview

The analysis relies on several key Python libraries:

**pandas:** Used for data loading, cleaning, manipulation, and preparing the data frames for both modeling and visualization.

**numpy:** Provides efficient numerical operations, particularly for handling arrays and numerical data.

**scikit-learn:** A core machine learning library.

**StandardScaler:** Used to scale features, a crucial step for the K-means clustering algorithm.

**KMeans:** The unsupervised learning model used to segment the data into distinct passenger clusters.

**RandomForestRegressor:** The supervised learning model used to predict passenger count and determine feature importance.

**statsmodels:** A library for statistical modeling.

**seasonal_decompose:** Used for the time-series analysis to break down the data into trend, seasonality, and residuals.

**matplotlib & seaborn:** Libraries used for generating the various charts and plots for the EDA and model visualization.


## Data Sources

The Air_Traffic_Pax_v3.csv dataset, a key component of this project, was compiled by integrating information from several public data sources to create a comprehensive view of San Francisco International Airport (SFO) air traffic.

**flysfo.com**: The primary source for all flight-level details, including Passenger Count, Flight Type, Terminal, and Boarding Area. This data forms the foundation of the project's analysis of SFO's operational metrics.

**data.gov**: A supplementary source used to augment and cross-reference the core airport data, ensuring a robust and reliable foundation for the analysis.

**OpenFlights.org**: The source for crucial airline and route-specific metadata, including flight_distance_km, num_routes, and fleet_size. This information is vital for the K-means clustering analysis, which segments routes based on their operational characteristics.

**Data.worldBank.org**: Provides the GDP (Gross Domestic Product) data, which is used as an external variable in the predictive model to help explain passenger traffic trends in relation to economic activity.


## Note

This project is a detailed case study in applying data science to a real-world business problem. While the Air_Traffic_Pax_v3.csv dataset is from a specific context (San Francisco International Airport), the analytical approach and workflow presented in this repository are replicable and adaptable to a wide range of business intelligence and predictive modeling tasks in various industries. The project emphasizes the importance of a structured analytical process, from understanding the raw data to building and interpreting complex models to provide actionable business insights.
