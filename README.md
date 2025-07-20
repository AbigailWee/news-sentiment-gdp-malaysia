# Leveraging News Sentiment to Forecast GDP's Demand Components: A Malaysian Case Study

## 📚 Introduction
This study examines the role of Mandarin news sentiment in forecasting Malaysia's GDP and its demand-side components—private investment, private consumption, imports, and exports. Given the delays in publishing key economic indicators, the research explores alternative methods for capturing economic sentiment through the analysis of Mandarin news articles. By analyzing these articles and applying machine learning models, the study aims to provide more timely and accurate forecasts of Malaysia’s GDP and its key economic components.

## 📋 Critical Discussion Points

### CHAPTER 1: INTRODUCTION

#### 📌 1.1 Problem Statements

>▪️ Macroeconomic indicators like GDP are reported with a 90-day delay in Malaysia, limiting timely decision-making.
>
>▪️ The COVID-19 pandemic highlighted the need for real-time economic insights, as traditional indicators like GDP were too slow to capture rapid economic changes.
>
>▪️ Survey-based indices like the Business Condition Index (BCI) and Consumer Sentiment Index (CSI) often provide incomplete or biased data during economic downturns due to low response rates.
>
>▪️ Most research focuses on English-language news sentiment, overlooking non-English sources like Mandarin, which are significant in Malaysia's multilingual context.
>
>▪️ This study focuses on the predictive power of Mandarin news sentiment for forecasting Malaysia’s GDP due to time and resource constraints.
>
>▪️ Although high-frequency indicators are used in nowcasting, this study applies them to a quarterly forecasting task based on the available data.

#### 📌 1.2 Project Questions

The questions that this study aims to address are outlined as follows:

>▪️ Does the news sentiment index computed in the study accurately reflect the BCI and CSI published by MIER?
>
>▪️ How does the performance of the Mandarin text-derived news sentiment compare to the English text-derived sentiment in the work of Chong et al. (2021)?
> 
>▪️ Which of the four demand-side components (private investment, private consumption, imports, and exports) of GDP exhibited a strong correlation with the newly constructed news sentiment index, and which showed a weak correlation?

###### ⚠️ Note: The work of Chong et al. (2021) can be found [here](https://www.bis.org/ifc/publ/ifcb57_17.pdf).

#### 📌 1.3 Aim and Objectives

**Aim:**  

> To assess the role of Mandarin news sentiment in forecasting Malaysia's GDP and its four demand components—private investment, private consumption, imports, and exports—using machine learning techniques.

**Objectives:**  

> 1. To evaluate the effectiveness of Mandarin news sentiment in predicting the Business Confidence Index (BCI) and Consumer Sentiment Index (CSI).
>  
> 2. To compare the predictive performance of Mandarin news sentiment with English news sentiment as reported by previous studies.
> 
> 3. To determine the correlation between GDP’s demand-side components and the constructed news sentiment index.

#### 📌 1.4 Scope of the Study

> ▪️ This study examines the use of Mandarin news sentiment to forecast Malaysia’s quarterly GDP and its demand-side components: private consumption, private investment, imports, and exports.
>
> ▪️ The dataset includes 3,361 economic articles scraped from See Hua Daily News, covering the period from Q1 2022 to Q4 2023.
>
> ▪️ Sentiment analysis is conducted using a dictionary-based approach, tailored for economic contexts, due to the lack of publicly available pretrained Mandarin sentiment models for Malaysia.
>
> ▪️ The computed sentiment index is benchmarked against official indicators: Business Conditions Index (BCI), Consumer Sentiment Index (CSI), and macroeconomic statistics from the Department of Statistics Malaysia (DOSM).
>
> ▪️ Multiple machine learning models—including LASSO, Ridge, SVR, Random Forest, and XGBoost—are employed using a 4-quarter rolling window forecasting framework.
>
> ▪️ The study does not imply causality between sentiment and economic outcomes; it aims to assess predictive power within a limited, multilingual news context.



#### 📌 1.5 Significance of the Study

>▪️ Fills a gap in sentiment analysis by focusing on Mandarin news in a multilingual, multiethnic context.
>
>▪️ Provides a benchmark for future research in multilingual economies exploring economic sentiment.
>
>▪️ Enhances local forecasting of macroeconomic variables using vernacular media sources.
>
>▪️ Supports policymakers in improving short-term economic forecasts specific to Malaysia’s unique dynamics.

---

### CHAPTER 2: LITERATURE REVIEW

Provides a foundation for understanding the scope of the study and highlights existing research gaps. It covers four main areas:

> 1.  Adoption of news sentiment for forecasting macroeconomic indicators like GDP growth, inflation, and unemployment.
>    
> 2.  Sentiment analysis of vernacular languages with a focus on Chinese, particularly in economic and financial contexts.
>    
> 3.  Application of machine learning models in sentiment analysis and their effectiveness in economic forecasting.
>   
> 4.  A review of the work by Chong et al. (2021), which forms the basis for this study.

#### 📌 2.1 Forecasting Key Economic Indicators through News Sentiments

>▪️ News sentiment has been widely used to forecast GDP, inflation, and unemployment.
>   
>▪️ Domain-specific sentiment tools are necessary, as generic models may not capture economic nuances.
>   
>▪️ Researchers recommend leveraging big data indicators and multilingual textual sources.

#### 📌 2.2 Multilingual Sentiment Analysis (Emphasis on Chinese Texts)

>▪️ Although sentiment analysis spans various languages, Chinese economic texts remain underexplored.
>    
>▪️ Studies suggest culturally sensitive models for real-time analysis, especially for platforms like Weibo.
>    
>▪️ There is a research gap in Chinese financial sentiment analysis, especially outside mainland China.

#### 📌 2.3 Review of Machine Learning Models for Sentiment Analysis

>▪️ Models such as Random Forest, Gradient Boosting, and LASSO excel in economic forecasting tasks.
>    
>▪️ Ensemble models often outperform single models, especially when handling high-dimensional, nonlinear data.

#### 📌 2.4 Chong et al. (2021) and News Sentiment for Macroeconomic Forecasting

>▪️ Chong et al. (2021) provide a benchmark for this study by using English news sentiment to nowcast GDP.
>    
>▪️ Their approach emphasizes multiple lexicons and refined sentiment scoring for Malaysian economic data.

---

### CHAPTER 3: PROJECT METHODOLOGY 

> ▪️ The study follows the Cross-Industry Standard Process for Data Mining (CRISP-DM), which includes six stages: Business Understanding, Data Understanding, Data Preparation, Modelling, Evaluation, and Deployment.
> 
> ▪️ The first stage of Business Understanding has been previously addressed in Chapter 1, covering the aims and objectives of the study.
>  
> ▪️ The deployment stage will not be included in this study, and details of the remaining four stages — Data Understanding, Data Preparation, Modelling, and Evaluation — will be further elaborated in Chapter 4.

---

### CHAPTER 4: IMPLEMENTATION

#### 📌 4.1 Data Collection Process

> ▪️ MIER Dataset: BCI and CSI data for 2022–2023 were purchased from the Malaysian Institute of Economic Research (MIER).
> 
> ▪️ Macroeconomics Dataset: Data for GDP, private consumption, private investment, imports, and exports were sourced from the Department of Statistics Malaysia (OpenDOSM).
> 
> ▪️ News Articles: A total of 3,361 articles from See Hua Daily News were scraped using ParseHub due to limitations with other news portals.

#### 📌 4.2 Initialization of the Data Analysis Process

> ▪️ Data Loading: Collected datasets (BCI, CSI, macroeconomic indicators, news articles) were loaded into Visual Studio Code for processing.

#### 📌 4.3 Initial Exploratory Data Analysis of the Textual Dataset

> ▪️ Exploration and Cleaning: The structure of the news articles dataset was explored, missing data was cleaned, and irrelevant columns were removed.
>  
> ▪️ Preliminary Dataset Structure: The data was reviewed after preliminary cleaning to confirm its readiness for further analysis.

#### 📌 4.4 Initial Exploratory Data Analysis of the Numerical Datasets

> ▪️ Exploration of BCI, CSI, and Macroeconomic Data: The structure of BCI, CSI, and macroeconomic datasets was examined. Outliers were checked, and summary statistics were generated for further analysis.

#### 📌 4.5 Preprocessing Steps for the Textual Dataset

> ▪️ Tasks: Data cleaning, including stripping whitespace, converting Chinese dates to standard format, and performing text normalization.
> 
> ▪️ Text Processing: Sentiment dictionary and stop words were loaded, and text preprocessing was completed to prepare the data for sentiment analysis.

#### 📌 4.6 Exploratory Data Analysis (EDA) of the Preprocessed Textual Dataset

> ▪️ Verification and Saving: The preprocessed textual data was verified and saved in CSV format for further analysis.

#### 📌 4.7 Computation of the News Sentiment Index

> ▪️ Sentiment Analysis: The sentiment index was calculated by analyzing the sentiment scores of each news article.
> 
> ▪️ Sentiment Score Calculation: Each article's sentiment score was determined by subtracting the count of negative words from positive words, normalized by the total word count, and multiplied by 1000 to create a normalized score.
> 
> ▪️ Normalization: This calculation results in a net count per thousand words, where values above 100 indicate positive sentiment and values below 100 indicate negative sentiment.
> 
> ▪️ Quarterly Index: The sentiment scores were aggregated on a quarterly basis, scaled by the number of articles per quarter, and averaged across all news portals to create the final quarterly sentiment index.

#### 📌 4.8 Nowcasting BCI and CSI Figures Using the News Sentiment Index

> ▪️ Data Preparation: The sentiment index was merged with BCI and CSI data for regression analysis.
> 
> ▪️ Time Series and Regression: Time series plotting and regression analysis were conducted to nowcast BCI and CSI values. Actual vs predicted values were plotted, and multicollinearity checks were performed to ensure model validity.

#### 📌 4.9 Evaluating the Pearson Correlation Between the Macroeconomics Variables and the News Sentiment Index

> ▪️ Data Preparation: Quarterly sentiment index data was loaded from the CSV file. It was then merged with the macroeconomic data (imports, exports, GDP, private consumption, private investment) based on Date and Quarter columns.
> 
> ▪️ Pearson Correlation: Pearson correlation coefficients were computed to evaluate the relationship between the sentiment index and each macroeconomic variable.

#### 📌 4.10 Modelling Process for Forecasting the Five Target Variables Using Machine Learning Models

**Modelling without Hyperparameter Tuning:**

> ▪️ Initialization: RMSE and MAE functions were defined. Models such as Linear Regression, LASSO, Ridge, SVR, Random Forest, and XGBoost were used for forecasting. The data was prepared with a 4-quarter rolling window approach.
> 
> ▪️ Rolling Window Approach: This approach was applied to train and test the models across forecast horizons (1, 2, 3 quarters). RMSE and MAE were computed and stored for each model and variable.
> 
> ▪️ Results Display: RMSE and MAE ratios were plotted and analyzed for each model and forecast horizon.

**Modelling with Hyperparameter Tuning:**

> ▪️ Initialization and Tuning: Hyperparameter tuning using Grid Search was conducted for LASSO, Ridge, SVR, Random Forest, and XGBoost. Best models were then used in a rolling window approach.
> 
> ▪️ Results Display: Performance evaluation based on RMSE and MAE ratios was presented, comparing tuned models to baseline results.

---

### CHAPTER 5: RESULTS AND ANALYSIS

#### 📌 5.1 Nowcasting the BCI and CSI Figures Using the News Sentiment Index

![Screenshot 2024-10-24 201102](https://github.com/user-attachments/assets/dd0107d7-250e-4d76-a0ca-5b1ce5f745b6)

> ▪️ Time Series Plot: Shows the relationship between the News Sentiment Index and MIER’s BCI and CSI from 2022 Q1 to 2023 Q4. The sentiment index trends upward with some alignment to BCI, but both indices exhibit volatility, with weak correlations between sentiment and the economic indices.

![Screenshot 2024-10-25 175656](https://github.com/user-attachments/assets/54711f19-6777-4786-9088-a7efe026c846)

![Screenshot 2024-10-24 201440](https://github.com/user-attachments/assets/da1b06e8-5c6a-4289-bb93-bf9ac1f9b96d)

> ▪️ Regression Output for Nowcasting BCI: The regression model explained 69.7% of the variance in BCI values (R-squared = 0.697). The quarterly sentiment index negatively correlated with BCI, which was unexpected. Lagged BCI was not significant.

![Screenshot 2024-10-25 175507](https://github.com/user-attachments/assets/4a1a9478-b67c-46ac-b442-12d26ddb1968)

![Screenshot 2024-10-24 201901](https://github.com/user-attachments/assets/a942a265-7426-4761-b5af-37829155f76f)

> ▪️ Regression Output for Nowcasting CSI: The model for CSI performed poorly with very weak correlations, indicating the sentiment index was not predictive of consumer sentiment.

#### 📌 5.2 Forecasting the Five Target Variables Using the News Sentiment Index

![Screenshot 2024-10-25 180034](https://github.com/user-attachments/assets/e9e20059-78b0-41cb-814c-bf032aa78438)

> ▪️ Pearson Correlation: Correlation between the sentiment index and the five macroeconomic variables (GDP, private consumption, private investment, imports, and exports) was calculated. Most correlations were weak or negative.
> 
> ▪️ Performance Evaluation for Machine Learning Models Without Hyperparameter Tuning: Various models (LASSO, Ridge, Random Forest, etc.) were used in a rolling window approach to forecast the five variables. The results were evaluated using RMSE and MAE ratios.
> 
> ▪️ Performance Evaluation for Machine Learning Models With Hyperparameter Tuning: Hyperparameter tuning improved performance in some models. LASSO and Random Forest performed well, especially for private consumption and private investment.

---

### CHAPTER 6: DISCUSSION AND CONCLUSIONS

#### 📌 6.1 Discussion of Nowcasting Findings

> ▪️ BCI: The sentiment index significantly predicted BCI, confirming its alignment with business confidence. No multicollinearity issues were found.
> 
> ▪️ CSI: The sentiment index failed to predict CSI, showing weak correlation and poor model performance, similar to previous studies.

#### 📌 6.2 Discussion of Forecasting Findings

> ▪️ Pearson Correlation: Sentiment had weak or negative correlations with most macroeconomic variables, particularly GDP and imports.

#### 📌 6.3 Conclusions

> ▪️ Mandarin-based news sentiment proved useful for forecasting business confidence (BCI) but was less effective for predicting consumer sentiment (CSI) and other macroeconomic variables like GDP and imports.
> 
> ▪️ While LASSO and Random Forest models performed well, particularly for private consumption and investment, the overall weak correlations highlight the limitations of using a single news source and a short timeframe.
> 
> ▪️ Future research should expand data sources, extend the analysis period, and explore additional models to improve forecasting accuracy across more economic variables.

---

#### ⚠️ Note: Mojibake may occur with "preprocessed_data.csv" and "See Hua (New).csv."

To fix it, go to Data > Get External Data > From Text, select the file, and choose Unicode (UTF-8) encoding in the import wizard to display Mandarin characters correctly.


