# **Analysis of Overall Healthcare Worldwide**

![Project Logo](https://www.e-ir.info/wp-content/uploads/fly-images/84328/Screenshot-2020-05-22-at-19.22.11-807x455-c.jpg)

## **Overview**

Our research project aims to conduct a comprehensive analysis of global health data to identify areas in greatest need of assistance or aid from organizations like the World Health Organization (WHO). Additionally, we seek to identify countries that demonstrate exemplary health outcomes and practices, serving as valuable lessons for global health improvement efforts. By analyzing various datasets and employing statistical methods, we will investigate key factors such as medical personnel prevalence, GDP per capita, and mortality rates. Through this research, we aim to contribute to the understanding of global health disparities and provide insights to support evidence-based decision-making in healthcare planning and resource allocation.

> **Research Question:**  
> Based on comprehensive analysis of general health data, which areas of the world are in greatest need of assistance or aid from the World Health Organization (WHO) and other organizations, and which countries demonstrate exemplary health outcomes and practices that can serve as valuable lessons for global health improvement efforts?

The slide deck of our presentation can be found as a PDF, titled: [Presentation - Analysis of Overall Healthcare Worldwide.PDF](https://docs.google.com/presentation/d/1ocTOHkDrqGDJFO85Cjwz38St5kXDhVix88cvsFs2HfM/edit#slide=id.g252acccf8a5_0_18).

---

## **Instructions**

### **Data Sets**

Data sets were obtained from the following websites:  
- Kaggle  
- World Health Organization (WHO)  
- World Development Indicator (WDI)  
- Google Developers

The data sets included the following information:  
- **GDP**  
- **Life Expectancy**  
- **Medical Doctor Numbers**

---

### **Data Cleaning**

Data cleaning can primarily be found in Jupyter's notebook **`GDP_vs_life_expectancy.ipynb`**. The data cleaning process included the following steps:

- **Years:** 2015 to 2019.  
- Countries that did not have **Life Expectancy** for all analyzed years were excluded from the analysis.  
- Countries that did not have Male/Female ratio to calculate Life Expectancy for the entire population were assigned **50%**.  
- Life Expectancy for the entire population was calculated as a **weighted average** between Male Life Expectancy and Female Life Expectancy.  
- Data frame that contains information by country with averaged information across the analyzed years has **246 countries**.  
- For the number of Medical Doctors, a portion of the countries were filtered out from the original data set because of missing values, bringing the dataset to the size of **~150 countries**.

---

## **Analysis**

### **GDP and Medical Doctors**

The purpose of this analysis is to find out the correlation between **GDP per Capita** and medical resources per capita, and correlation between **GDP per Capita** and **Life Expectancy**. Then find the difference between the **top 20** and **bottom 20** nations. This analysis will help to understand why countries with higher GDP have higher life expectancy.

- The code for this analysis is in **`GDP_vs_life_expectancy.ipynb`**.  
- The dataframes used in this analysis are **`totalavgfilter.csv`** and **`world-population-by-countries-dataset.csv`**.  
- The **Pearson correlation** test was performed for understanding correlativeness between two datasets. After normalizing the dataset, a **log transformation** was performed when appropriate.  
- By comparing the GDP per capita and life expectancy column, it returns a correlation coefficient of **~0.83** (example result after log-transform), indicating a positive relation between GDP and life expectancy.  
- The correlation test between GDP per capita and medical doctors per capita returns a correlation coefficient of **~0.72**, demonstrating a strong relation between the two features.

---

## **References**

The datasets were taken from the following sources:  
- [World Bank](https://data.worldbank.org/indicator/SP.DYN.AMRT.FE)  
- [Kaggle](https://www.kaggle.com/datasets/paultimothymooney/latitude-and-longitude-for-every-country-and-state)  
- [World Population Dataset](https://www.kaggle.com/datasets/kiranshahi/life-expectancy-dataset?datasetId=1980580&sortBy=dateRun&tab=profile)
