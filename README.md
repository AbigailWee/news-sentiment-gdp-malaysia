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

> ▪️ This study explores how Mandarin news sentiment can forecast Malaysia’s GDP and its demand components: private investment, consumption, imports, and exports.
>
> ▪️ It uses Mandarin articles from See Hua Daily News covering Q1 2022 to Q4 2023.
>
> ▪️ Only one news source is analyzed, which may introduce bias but still allows useful insights.
>
> ▪️ A dictionary-based sentiment method is used due to limited Mandarin models available.
>
> ▪️ Sentiment scores are compared with official indicators like BCI, CSI, and DOSM macroeconomic data.
>
> ▪️ Machine learning models such as LASSO, Ridge, SVR, Random Forest, and XGBoost are applied using a rolling window approach.
>
> ▪️ The study addresses the lack of non-English sentiment analysis in Malaysia’s multilingual context.



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

>▪️ The study adopts the Cross-Industry Standard Process for Data Mining (CRISP-DM), consisting of six stages: Business Understanding, Data Understanding, Data Preparation, Modelling, Evaluation, and Deployment.
>
>▪️ Business Understanding is covered in Chapter 1. This chapter focuses on the Data Understanding, Preparation, Modelling, and Evaluation stages.
>
>▪️ Deployment is excluded due to scope limitations.

---

### CHAPTER 4: IMPLEMENTATION

#### 📌 4.1 Data Collection Process

>▪️ BCI and CSI were sourced from the Malaysian Institute of Economic Research (MIER).
>    
>▪️ Macroeconomic data (GDP, consumption, investment, imports, exports) was obtained from OpenDOSM.
>    
>▪️ A total of 3,361 Mandarin articles were scraped from See Hua Daily News using ParseHub.

#### 📌 4.2 Initialization of the Data Analysis Process

>▪️ All datasets were loaded into Visual Studio Code for cleaning and analysis.

#### 📌 4.3 Initial Exploratory Data Analysis of the Textual Dataset

>▪️ The article dataset was cleaned by removing missing values and irrelevant columns.
>    
>▪️ Structural checks were conducted to ensure readiness for analysis.

#### 📌 4.4 Initial Exploratory Data Analysis of the Numerical Datasets

>▪️ Summary statistics and outlier detection were conducted on the BCI, CSI, and macroeconomic datasets.

#### 📌 4.5 Preprocessing Steps for the Textual Dataset

>▪️ Preprocessing included whitespace stripping, date conversion, and normalization.
>    
>▪️ A sentiment dictionary and stopword list were applied to prepare for sentiment scoring.

#### 📌 4.6 Exploratory Data Analysis (EDA) of the Preprocessed Textual Dataset

>▪️ Preprocessed text was verified and saved as a CSV file for sentiment analysis.

#### 📌 4.7 Computation of the News Sentiment Index

>▪️ Sentiment score = (positive word count – negative word count) / total words × 1000.
>    
>▪️ Quarterly sentiment index = mean of article-level scores, scaled by article count.

#### 📌 4.8 Nowcasting BCI and CSI Figures Using the News Sentiment Index

>▪️ Regression models were developed to nowcast BCI and CSI using sentiment indices.
>    
>▪️ Multicollinearity checks and time series plots were used for evaluation.

#### 📌 4.9 Evaluating the Pearson Correlation Between the Macroeconomic Variables and the News Sentiment Index

>▪️ The sentiment index was merged with macroeconomic data based on quarter and year.
>    
>▪️ Pearson correlation coefficients were computed to assess relationships.

#### 📌 4.10 Modelling Process for Forecasting the Five Target Variables Using Machine Learning Models

**Without Hyperparameter Tuning:**

>▪️ Linear Regression, LASSO, Ridge, SVR, Random Forest, and XGBoost were used.
>    
>▪️ Models used a 4-quarter rolling window.
>    
>▪️ Evaluation was based on RMSE and MAE.

**With Hyperparameter Tuning:**

>▪️ Grid Search optimized the parameters of each model.
>    
>▪️ Tuned models were re-evaluated and compared against baselines.

---

### CHAPTER 5: RESULTS AND ANALYSIS

#### 📌 5.1 Nowcasting the BCI and CSI Figures Using the News Sentiment Index

>▪️ The sentiment index tracked BCI reasonably well but not CSI.
>    
>▪️ The BCI model achieved R² = 0.697 with a negative coefficient for the sentiment index.
>    
>▪️ CSI model showed weak correlation and low predictive value.

#### 📌 5.2 Forecasting the Five Target Variables Using the News Sentiment Index

>▪️ Pearson correlations with GDP and imports were weak or negative.
>    
>▪️ Without tuning: Random Forest and LASSO showed promise for investment and consumption.
>    
>▪️ With tuning: Model performance improved, particularly for private consumption.

---

### CHAPTER 6: DISCUSSION AND CONCLUSIONS

#### 📌 6.1 Discussion of Nowcasting Findings

>▪️ The sentiment index was a significant predictor for BCI but not for CSI.
>    
>▪️ Findings align with literature showing weak consumer sentiment modeling.

#### 📌 6.2 Discussion of Forecasting Findings

>▪️ Sentiment index correlations with GDP, imports, and exports were weak or inconsistent.
>    
>▪️ LASSO and Random Forest models provided better performance for investment and consumption.

#### 📌 6.3 Conclusions

>▪️ Mandarin sentiment can help forecast BCI but is less effective for broader macroeconomic indicators.
>    
>▪️ Model performance was limited by single-source data and short study period.
>    
>▪️ Future work should integrate multiple news sources and explore newer models.

---

#### ⚠️ Note: Mojibake may occur when opening "preprocessed_data.csv" or "See Hua (New).csv."

     ➤ To fix: Use Excel > Data > Get External Data > From Text > Select file > Choose "Unicode (UTF-8)" encoding.

