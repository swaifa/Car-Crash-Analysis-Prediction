About The Project 
---
This project analyzes historical car crash data in British Columbia to predict high-risk locations for future incidents and recommend remedies for few defined cases. The system is built using Python, Apache Spark, and PySpark.ML for data processing and machine learning. The results are visualized using Seaborn, Folium, and Matplotlib for intuitive insight presentation.

Data Engineering
--
In the Data Engineering process, I've focused on extracting, transforming, and loading (ETL) data from various sources to prepare it for machine learning and analysis. The data engineering pipeline is broken down into multiple stages and includes files for geocoding, cleaning, merging, and producing data for the machine learning models.

Datasets Used
----
The key datasets used in this project are as follows:

1/ TAS Data (Traffic Accident System Data): Contains details about where and how accidents happened in British Columbia (BC).


2/ ICBC Data (Insurance Corporation of British Columbia): Contains historical accident data that includes attributes such as location, weather, time, and crash severity.

ETL Process 
---

I've performed several transformation steps to clean, standardize, and enrich the crash datasets:

1/ Standardizing Column Names: Ensures consistency across all datasets (TAS, ICBC, weather, traffic).

2/ Feature Extraction: Extracts relevant features like crash severity, time of day, weather descriptions, and road conditions.

3/ Imputation: Missing values in numeric and categorical fields are imputed using appropriate statistical methods.

Data Exloration Process
---
Matplotlib and Seaborn is used to visualize the cleaned data to understand what kind of model can be used and for what objective. The visualizations are a part of the engineering process. 

Machine Learning (Hotspot Classification - merged_ml.ipynb)
---
This project uses supervised learning to predict crash severity risk at specific locations and times. The model is trained using historical crash data enriched with weather and traffic context. The core model is a Random Forest Classifier, chosen for its robustness and interpretability. However, a Multi-Layer Perceptron was also trained and tested.

After training, the model generates crash risk scores for location-time combinations, which are used to label zones as:

1/ Low risk: Low probability of crash occurrence

2/ Moderate risk: Some crash indicators present

3/ High risk: Strong indicators of upcoming crash risk

An interactive map is saved as an HTML file to visualize how the model classfies hotspots (hotspot-heatmap.html). 

Machine Learning (Remedy Recommendation - model4.ipynb)
--
A decision tree model with user-defined cases is used to recommend remedies for certain situations that contribute to a hotspot being 'hot'. 

Results
---
1/ Accuracy of 97% is achieved in Hotspot classification.

2/ The recommendation model runs with an accuracy of 77% with a scope of improvement with other user-defined situations. 

3/ Visualizations along with data exploration process help with understanding a trend between car crashes in BC. 

Future Improvements
--
1/ Develop a dashboard for the visualizations using Tableau or Power BI

2/ Start predicting on real-time data using API's and Kafka. 








