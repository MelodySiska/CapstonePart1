*Capstone Project: Analysis of LWBS % and Crowding in a Pediatric Emergency Department*  

Project Overview
This project aims to analyze the factors that contribute to higher Left Without Being Seen (LWBS) rates in a pediatric emergency department. Specifically, the analysis focuses on the impact of weekly patient arrivals and crowding, measured by the number of hours where the Pediatric Emergency Department Occupancy Scale (PEDOCS) exceeds 140. Through various techniques such as regression analysis, correlation heatmaps, and neural network models (LSTM), this project seeks to uncover key drivers of LWBS and provide actionable insights for managing patient flow and improving care quality.

Research Question
The main research question guiding this analysis is: How do weekly arrivals and crowding, as measured by PEDOCS > 140, influence LWBS rates in the emergency department?

Goals:
To assess the correlation between crowding and LWBS.
To predict future LWBS rates based on historical data using regression and machine learning techniques.
To evaluate the effectiveness of different intervention strategies on reducing LWBS rates.
Data Sources
The dataset used in this analysis is based on historical records from a pediatric emergency department, specifically focusing on:

Weekly Arrivals: The number of patients arriving at the ED each week.
LWBS %: The percentage of patients who left the ED without being seen each week.
'# Hrs > 140: The number of hours in a week where PEDOCS exceeded 140, indicating high levels of crowding.
Other Variables: Additional variables such as sedation count, STS activation count, and usage of the overflow area ("Team5").
Dataset Structure:
Week Begin	# Hrs > 140	Weekly Arrivals	LWBS %	Sedation Count	STS Activation Count	Team5 Usage
2023-08-13	0	976	5.53%	41	69	5
...	...	...	...	...	...	...
Techniques and Models Used
1. Exploratory Data Analysis (EDA):
Line Graphs: Visualized trends in weekly arrivals, LWBS %, and # Hrs > 140 to explore their relationships over time.
Scatter Plots: Investigated pairwise relationships between weekly arrivals, crowding, and LWBS %.
Correlation Heatmap: Assessed the strength of relationships between variables using a correlation matrix.
2. Regression Analysis:
OLS Regression: Built Ordinary Least Squares (OLS) regression models to quantify the impact of weekly arrivals and crowding on LWBS %.
Lasso and Ridge Regression: Applied regularization techniques to prevent overfitting and refine model coefficients.
3. Neural Networks (LSTM):
LSTM Model: Used Long Short-Term Memory (LSTM) networks to predict future LWBS % based on historical patterns in weekly arrivals and PEDOCS scores.
Model Performance: Compared LSTM results with traditional regression approaches using metrics such as Mean Squared Error (MSE).
4. Intervention Effectiveness:
Pre- and Post-Intervention Analysis: Compared LWBS % and crowding before and after interventions aimed at reducing patient flow issues and managing crowding.
Key Findings
Crowding is a Key Driver of LWBS:

The regression models demonstrated that the number of hours where PEDOCS exceeded 140 (# Hrs > 140) was the most significant predictor of LWBS %. Each additional hour of crowding resulted in a measurable increase in the percentage of patients leaving without being seen.
Weekly Arrivals Have a Smaller Impact:

While there is some correlation between weekly arrivals and LWBS %, the effect of arrivals on LWBS is much weaker compared to crowding. This suggests that managing crowding (e.g., using overflow areas or increasing staff flexibility) may be more impactful than simply managing arrivals.
LSTM Performance:

The LSTM model showed promising results in forecasting future LWBS % based on past trends, but further tuning of hyperparameters is needed to improve accuracy. The LSTM approach provides a time-sensitive analysis that complements the regression models.
Intervention Success:

The pre- and post-intervention analysis revealed that the strategies implemented (e.g., expanding the use of Team5) were effective in reducing both crowding and LWBS rates.
