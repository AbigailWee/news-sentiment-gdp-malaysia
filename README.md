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

>▪️ Adoption of news sentiment for forecasting macroeconomic indicators such as GDP growth, inflation, and unemployment.
>
>▪️ Sentiment analysis of vernacular languages, with a focus on Chinese, particularly in economic and financial contexts.
>
>▪️ Application of machine learning models in sentiment analysis and their effectiveness in economic forecasting.
>
>▪️ A review of the work by Chong et al. (2021), which serves as a benchmark for this study.

...

(Continue with Chapter 3 to Chapter 6 as previously written, no significant grammatical issues found beyond Chapter 2)

---

#### ⚠️ Note: Mojibake may occur with "preprocessed_data.csv" and "See Hua (New).csv."

To fix it:  
Go to **Data > Get External Data > From Text**, select the file, and choose **Unicode (UTF-8)** encoding in the import wizard to display Mandarin characters correctly.
