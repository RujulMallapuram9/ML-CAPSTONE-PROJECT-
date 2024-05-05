# ML-CAPSTONE-PROJECT-
Prediction and Forecasting of How Petroleum Sector effects GDP of India
1.	INTRODUCTION:

The petroleum sector plays a pivotal role in shaping the economic landscape of nations worldwide, and India is no exception. With its significant contribution to the Gross Domestic Product (GDP), the petroleum sector stands as a critical determinant of India's economic growth trajectory. Understanding the intricate relationship between the petroleum sector and India's GDP is essential for policymakers, economists, and industry stakeholders alike. In this study, we delve into the Impact of the Petroleum Sector on India's GDP, aiming to unravel the complex dynamics that underpin this relationship. Through a comprehensive analysis of relevant economic indicators and Machine modeling techniques, we seek to shed light on the extent to which the performance of the petroleum sector influences India's overall economic prosperity. By exploring key facets such as exports, domestic production, and energy consumption patterns, we aim to provide valuable insights that can inform strategic decision-making and policy formulation in the energy sector and beyond.

2.	PROBLEM STATEMENTS:

1.	Impact of Petroleum Exports on GDP: Analyze the relationship between exports of petroleum-related goods and services and India's GDP growth over time.

2.	Electricity Production from Oil and Economic Growth: Investigating how the proportion of electricity production from oil sources correlates with India's GDP, assessing whether increased reliance on oil for electricity affects economic performance.

3.	Oil Rents and Economic Stability: Examine the relationship between the percentage of GDP generated from oil rents (e.g., oil extraction revenues) and overall economic stability, exploring whether fluctuations in oil revenues impact GDP growth.

4.	Fuel Imports and Trade Balance: Assess the effect of fuel imports on India's trade balance and GDP, considering whether increased fuel imports contribute to trade deficits or surpluses and how this affects economic growth.


3.	DATASET DESCRIPTION:

1.	YEAR: This column represents the year of the data observation.

2.	GDP (current US$): This column denotes the Gross Domestic Product (GDP) of India in current US dollars for each corresponding year. GDP is a measure of the economic performance of a country and represents the total value of all goods and services produced within its borders.

3.	Exports of goods and services (current US$): This column indicates the total value of goods and services exported by India in current US dollars for each year. It reflects the country's international trade activities and export earnings.

4.	Electricity production from oil sources (% of total): This column represents the percentage of total electricity production in India that comes from oil sources. It provides insight into the energy composition of India's electricity generation infrastructure and its reliance on oil for power generation.

5.	Oil rents (% of GDP): This column indicates the percentage of GDP derived from oil rents, which typically include revenues from oil extraction activities. It reflects the contribution of the oil sector to India's overall economic output.

6.	Fuel imports: This column denotes the value of fuel imports (such as petroleum products) by India in current US dollars for each year. It indicates the country's dependence on imported fuel to meet its energy needs.

7.	Fossil fuel energy consumption (% of total): This column represents the percentage of total energy consumption in India that comes from fossil fuels. It provides insights into the country's energy consumption patterns and the extent of reliance on fossil fuels for energy production.

This dataset gives us a detailed look into how India's economy and energy usage have evolved over time. By examining key indicators like GDP, exports, electricity generation from oil, and fuel imports, we can better understand India's economic growth and its relationship with the global energy market. These insights help us grasp the country's economic progress and energy needs, guiding decisions for a sustainable future.








4.	DATA PREPROCESSING AND EXPLORATORY DATA ANALYSIS:

1.	DESCRIPTIVE STATISTICS:

   ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/4d8b817b-5f29-457b-8a1f-db093f19d4bb)

 
3.	CHECKING FOR NULL VALUES:

   ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/10edbddc-796a-4e98-8224-74ca1e942171)

 
There were 18 null values found in Electricity production from oil sources (% of total), 3 in Oil rents (% of GDP)  and 19 in Fossil fuel energy consumption (% of total).




3.	FILLING THE NULL VALUES:

   ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/a7c70efc-2841-43c8-ab1a-00a59a3d6b43)

 
We filled the null values using forward and backward fill.

4.	TEST FOR STATIONARITY OF DATA:

   ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/ed0b91c2-faf1-4492-9b91-7c4506fe5855)


 
We conducted the Augmented Dickey-Fuller Test on all the variables to check if they are stationary or not, all the variables were non-stationary.

5.	DIFFERENCING TO MAKE DATA STATIONARY:

 ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/42cc9eea-39f5-4c0c-8bbd-1aa39e6d6735)

After taking the third ordered difference the data was stationary.

![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/26a2d2ec-4871-47a9-aa83-6249066a7c59)

 

7.	CORRELATION MATRIX:

![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/7e4dd402-4aec-4614-b9be-d29d25ed50a6)

 
The analysis shows a strong link between a country's GDP and its exports (0.69). Countries that produce more goods and services tend to have larger economies. There's also a connection between oil revenue and fuel imports (0.26), and a weak negative link between exports and reliance on fossil fuels (-0.16).

7.	TESTS FOR MULTICOLLINEARITY:

![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/2f320cde-7321-4663-9749-6711a809d483)

 
GDP (current US$): The VIF value is 4.108, indicating a moderate level of multicollinearity with other predictor variables.

Exports of goods and services (current US$): The VIF value is 4.273, also indicating a moderate level of multicollinearity with other predictor variables.

Electricity production from oil sources (% of total): The VIF value is 1.204, which is relatively low and suggests minimal multicollinearity with other predictor variables.

Oil rents (% of GDP): The VIF value is 1.326, indicating minimal multicollinearity with other predictor variables.
Fuel imports: The VIF value is 1.232, suggesting minimal multicollinearity with other predictor variables.

Fossil fuel energy consumption (% of total): The VIF value is 1.237, also indicating minimal multicollinearity with other predictor variables.

Overall, the VIF values for most of the features are low, indicating minimal multicollinearity among the predictor variables.

8.	DISTRIBUTION OF DATA:
Most of the variables were not normally distributed and showed a trend in \their distribution.

  ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/eb31048d-e703-4295-b7bc-57299467dd71)

  ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/4cd5fe94-887b-413d-b76e-d22bcf516380)

  ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/95626e64-17b1-4cbb-abca-a1239f7b3c8a)

  ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/d4be2ab5-4a92-4c77-9bad-730d5a3b8bed)

  ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/33e65cc3-15de-4e80-916c-30fdd134b06c)

  ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/aec8fc9e-0a29-4444-99cf-f44c7af038b2)
  
9.	FORMAL TEST FOR NORMALITY:
Most of the variables were not normally distributed.

![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/72bdbad6-dddb-4ada-9ce2-0c3279390a5b)

 

10.	INTERACTIVE LINE PLOT:
Interactive Line Plot was made to understand the relationship between variables of choice and plot was designed such that time wise analysis can also be done.

![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/692acbd1-006c-4ffb-8071-fcfd00e7eafe)

![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/b1e36098-2036-48aa-8355-f583e7c99bdd)


11.	PAIR PLOTS:
Pair scatter plots were plotted for all variables, which helped us understand how they interact with each other.
 

![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/ddf7e648-9fe7-4d6d-9a41-6a929652cc46)



12.	STANDARDIZATION AND NORMALIZATION OF DATA:

The data had to be standardized to get the variables on the same scale and also normalized as it is easier and better for prediction.

![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/6014101e-fb9c-4176-a5ca-115e334908bb)


13.	PRINCIPAL COMPONENT ANALYSIS (PCA):

Principal Component Analysis (PCA) was utilized to reduce the dimensionality of the economic data and extract key features. This technique identifies a smaller set of uncorrelated variables (principal components) that capture the most significant economic patterns. Analyzing these PCs allows for a more concise examination of the interplay between various economic forces.

![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/d14f19a5-f15c-4555-8add-fba5f8538901)

 
The selection of the optimal number of principal components (PCs) for further analysis was guided by the scree plot. This graphical tool depicts the explained variance captured by each PC in descending order. A scree plot typically exhibits a sharp initial descent followed by a flattening of the curve. The "elbow" formed at this inflection point signifies the point where subsequent PCs contribute minimal additional variance. By retaining PCs preceding this elbow, we ensure that the most informative features of the original data are captured in a reduced dimensionality, facilitating more efficient analysis without compromising the integrity of the underlying economic relationships.

   ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/6f1a77f6-a5df-4a95-9347-4e859d6f4a9c)


5.	MODEL BUILDING AND MODEL BUILDING:

a.	 Prediction

In our study on the impact of the petroleum sector on India's GDP, we undertook a comprehensive analysis employing various regression models to understand the relationship between key economic indicators and GDP. Our investigation involved the evaluation of six regression models: Decision Tree, Random Forest, Gradient Boosting Machine (GBM), Support Vector Machine (SVM), K-Nearest Neighbors (KNN), and Linear Regression.

 ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/4ba28e98-4a22-49ed-8fff-91716f6ea005)


Hyperparameter Tuning:
To ensure optimal model performance, we utilized hyperparameter tuning techniques via GridSearchCV. This approach systematically explores a predefined grid of hyperparameters to identify the most suitable configuration for each model. For instance, in Decision Tree, we experimented with different maximum depths, while in Random Forest, we varied the number of estimators. Similarly, for GBM, we adjusted the number of estimators and learning rate, and for SVM, we tuned the regularization parameter (C) and kernel choices. KNN was optimized by varying the number of neighbors. Linear Regression, being a simpler model, does not require hyperparameter tuning.
 
![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/8d18c94c-d341-4d0f-a912-364f4ba497ac)


Best Estimators and Model Selection:
Following hyperparameter tuning, we identified the best estimators for each model based on mean squared error (MSE) metrics obtained through cross-validation. Through rigorous evaluation, we determined Linear Regression to be the most suitable model for our analysis.

 ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/6437f2f5-a5fa-4bd6-b295-0f2f7b3d25c6)


Justification for the Chosen Model:
Linear Regression emerged as the optimal choice due to its superior performance across key evaluation metrics. It exhibited low training RMSE and reasonable test RMSE, suggesting its capability to predict GDP accurately. Furthermore, the high R-squared values on both training and test datasets indicate that the model explains a substantial portion of the variance in GDP. Notably, Linear Regression offers interpretability, facilitating a clear understanding of the relationship between economic indicators and GDP.

 
![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/e740ac66-b42f-46d8-ad15-8699cdb8f411)



GRAPH:
 
![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/91067851-6722-4b50-b259-92556fa655b9)


b.	Forecasting

![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/db74ef54-35ce-40e2-84dd-466b22c80e73)


GRAPH:
 
![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/603f7aa1-54be-4a94-ab53-a5ffec90fece)



6.	RESULTS AND DESCRIPTION:

Linear regression:

The Linear Regression model demonstrated strong predictive capability in both training and test datasets. With a training RMSE of 0.0275 and R2 of 0.9642, it effectively captured variations in the training data. Although the test RMSE increased slightly to 0.6659, and the R2 dropped to 0.6850, the model still exhibited significant predictive power on unseen data. These results indicate that while the model's performance slightly degraded on the test set, it remained effective in explaining variability and making accurate predictions.

 ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/7018f4eb-c567-4889-9ce9-611ec0d39fb4)


ARIMA Model:

The automatic selection process of an ARIMA (AutoRegressive Integrated Moving Average) model, optimizing based on the Akaike Information Criterion (AIC). The chosen ARIMA(4,0,1) model signifies four autoregressive (AR) terms, one moving average (MA) term, and no differencing (d=0). The 'intercept' coefficient represents the constant term. Coefficients for AR and MA terms are provided, alongside their standard errors, z-scores, and p-values. Further, goodness-of-fit metrics such as log likelihood, AIC, and BIC are presented. Diagnostic tests (Ljung-Box and Jarque-Bera) assess residuals for autocorrelation and normality assumptions, respectively.

 ![image](https://github.com/RujulMallapuram9/ML-CAPSTONE-PROJECT-/assets/118895292/d677b554-2ed1-4dba-9b6d-c19c23d986c0)



PROBLEM STATEMENT SOLUTIONS:

Impact of Petroleum Exports on GDP:
There is a positive relationship between petroleum exports and India’s economic growth.
Petroleum exports contribute to GDP growth in both the short run and long run.

Electricity Production from Oil and Economic Growth:
The report does not directly address this specific relationship.
However, India’s energy mix is still heavily reliant on coal, oil, and solid biomass.

Oil Rents and Economic Stability:
Oil rents as a percentage of GDP in India are around 0.3%.
While not a dominant factor, oil rents contribute to economic stability.

Fuel Imports and Trade Balance:
India’s high oil imports impact the trade balance.
Rising oil prices can lead to a wider trade deficit and affect GDP growth.


7.	RESULTS:

This comprehensive analysis delved into various economic dynamics, with a keen focus on understanding the intricate relationship between petroleum exports, oil rents, fuel imports, and India's overall economic performance. Through rigorous statistical modeling and forecasting techniques, we gained valuable insights that can inform strategic decision-making and policy formulation.

Predictive Modeling Insights:
Our study employed both Linear Regression and ARIMA models to elucidate the predictive capabilities of economic indicators. While Linear Regression effectively captured variations in the training data, the ARIMA model demonstrated superior performance in forecasting future trends. This distinction highlights the importance of selecting the appropriate modeling approach based on the nature and characteristics of the data.

Impact of Petroleum Exports on GDP:
Our analysis revealed a significant positive relationship between petroleum exports and GDP, indicating the substantial contribution of the petroleum sector to India's economic growth. This finding underscores the importance of fostering and leveraging the country's export potential in the petroleum industry to drive overall economic development.

Role of Oil Rents and Fuel Imports:
Oil rents were identified as contributing to economic stability, despite representing a relatively small percentage of GDP. However, the high dependence on fuel imports emerged as a critical concern, posing challenges to India's trade balance and potentially impacting GDP growth. Addressing this dependency and exploring avenues for diversifying energy sources could mitigate economic risks and enhance resilience.

Strategic Implications:
In conclusion, our analysis underscores the importance of strategic economic policies aimed at fostering sustainable growth and stability. By leveraging the positive impact of petroleum exports while addressing challenges associated with fuel imports, policymakers can steer the economy towards a path of diversified and resilient growth. Additionally, investments in alternative energy sources and infrastructural development can mitigate vulnerabilities and ensure long-term economic sustainability.

In summary, this study lays the groundwork for making well-informed decisions and shaping policies that aim to enhance India's economic performance and promote sustainable development amidst the ever-changing global landscape.
