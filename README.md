

# Analysis of FOMC Statements Using Topic Modeling and Sentiment Analysis

## Overview

This project explores the application of text mining techniques, specifically Topic Modeling via Latent Dirichlet Allocation (LDA) and Sentiment Analysis, to analyze Federal Open Market Committee (FOMC) statements. The primary goal is to uncover insights into the policy stance and sentiment reflected in these statements from 2015 to 2024, offering a quantitative and qualitative understanding of the Federal Reserve's communications over a significant period.

## Project Structure

- **`Code.ipynb`**: The Jupyter Notebook containing the implementation of text preprocessing, sentiment analysis, and topic modeling using Python. This script handles the entire pipeline from data collection to generating visualizations of the analysis results.
- **`Report.pdf`**: A detailed report documenting the methodology, analysis, and findings from the project. The report includes a comprehensive overview of the U.S. economy during the period studied, the steps taken for data preprocessing, and the results of the sentiment and policy stance analyses.

## Methodology

### Data Collection and Preprocessing

The project begins with the collection of FOMC statements from December 2015 to July 2024, sourced from the Federal Reserve's official website. These statements are critical as they communicate the Federal Reserve's monetary policy decisions and economic outlook.

- **Text Preprocessing**: The statements were processed using standard text preprocessing techniques, including lowercasing, punctuation removal, tokenization, and lemmatization. This ensures the text data is clean and standardized, which is crucial for accurate analysis.

### Sentiment Analysis

To quantify the sentiment in FOMC statements, a rule-based sentiment analysis approach was used:

- **Financial-Specific Lexicon**: The Loughran-McDonald sentiment word lists, specifically designed for financial text, were employed to capture the sentiment more accurately compared to general-purpose lexicons. The analysis focused on categorizing words into positive and negative sentiments, while excluding categories like litigious or uncertain terms to avoid diluting the sentiment scores.
- **Sentiment Scoring**: Each statement's sentiment was quantified by calculating the net sentiment score, which was normalized to fall between -1 and 1. This score provides a clear measure of the sentiment expressed by the FOMC over time.

### Policy Stance Analysis

The policy stance of the FOMC was analyzed using Topic Modeling:

- **Latent Dirichlet Allocation (LDA)**: LDA was applied to identify underlying topics within the FOMC statements. These topics were then interpreted as representing expansionary or contractionary policy stances.
- **Topic Identification and Refinement**: Topics were refined by removing high-frequency and low-frequency words to focus on the most informative terms. The LDA model then categorized the statements into different policy stances, which were normalized to a scale of -1 to 1 for easy interpretation.
- **Scoring Mechanism**: The final policy stance score was calculated by assessing the weighted probability of topics in each statement, providing a quantifiable measure of the Federal Reserve's policy direction over time.

## Results

### Sentiment Analysis

- **Event-Based Sentiment Trends**: The sentiment analysis revealed distinct trends corresponding to major economic events. For instance, sentiment sharply declined during the COVID-19 pandemic, reflecting the severe economic challenges faced during that period.
- **Financial-Specific Lexicon Effectiveness**: The use of a financial-specific lexicon allowed for a more nuanced understanding of the FOMC's sentiment, particularly in periods of economic uncertainty. This method provided a more accurate reflection of the cautious and often neutral tone of FOMC statements.

### Policy Stance Analysis

- **Evolution of Policy Stance**: The LDA-based analysis successfully tracked the evolution of the Federal Reserve's policy stance from gradual tightening post-Great Recession, to the emergency expansion during the COVID-19 pandemic, and the aggressive tightening in response to inflation concerns from 2022 onwards.
- **Comparison Across Periods**: The analysis highlighted differences in policy strictness across periods, with more aggressive measures observed in the post-2021 tightening phase compared to earlier periods.

## Discussion

### Alignment with Historical Events

The analysis results aligned well with significant economic events, such as the post-Great Recession recovery, the COVID-19 pandemic, and the subsequent inflationary period. These alignments validate the effectiveness of the methodologies used.

### Methodological Strengths

- **Sentiment Analysis**: The financial-specific lexicon provided a more accurate sentiment measure, particularly in a domain where neutral or cautious language is common.
- **Topic Modeling**: LDA effectively identified and categorized topics, offering a clear representation of the policy stance communicated in the FOMC statements.

### Limitations and Areas for Improvement

- **Contextual Nuances**: The rule-based sentiment analysis could be enhanced by incorporating machine learning models to better capture context and subtleties in language.
- **Granularity of Policy Stance**: The LDA model could be further refined to capture the varying degrees of policy strictness, particularly during periods of aggressive tightening or expansion.


