# The Impact of Sleep Quality on Daily Cognitive Performance

# Motivation

Sleep is a critical factor influencing cognitive performance, including attention, memory, decision-making, and problem-solving abilities. Despite the known importance of sleep, many individuals experience poor sleep quality due to lifestyle, stress, or environmental factors, which can negatively affect daily cognitive functioning.

This project investigates the relationship between sleep quality and daily cognitive performance. By tracking sleep metrics (duration, efficiency, wake after sleep onset, etc.) and assessing cognitive outcomes (reaction time, memory recall, attention tasks), we aim to quantify how variations in sleep impact cognitive function.

Using wearable devices (e.g., Apple Watch, Fitbit) and standardized cognitive tests, this project bridges physiological monitoring with behavioral analysis, providing insights for optimizing both sleep and daily mental performance.

# Objectives

1- **Track Sleep Quality**: Collect sleep data including total sleep time, sleep stages, and interruptions using wearable devices.

2- **Assess Cognitive Performance** : Conduct daily cognitive tests measuring reaction time, working memory, and attention.

3- **Analyze the Sleep–Cognition Relationship** : Use statistical and visual analyses to identify correlations between sleep metrics and cognitive performance.

4- **Develop Evidence-Based Recommendations**: Provide guidance on improving sleep to enhance cognitive functioning in daily activities.

# Dataset

The dataset consists of personal sleep and cognitive performance data collected over a 30-day period:
| Feature                                    | Description                                                                 |
|--------------------------------------------|-----------------------------------------------------------------------------|
| Total Sleep Time (hours)                   | Duration of nightly sleep                                                   |
| Sleep Efficiency (%)                       | Ratio of total sleep time to time in bed                                    | 
| Time in Deep Sleep (hours)	               | Duration of restorative sleep                                               |
| Time in REM Sleep (hours)                  | Duration of REM sleep, critical for memory consolidation                    |
| Wake After Sleep Onset (WASO, minutes)	   | Time spent awake during the night                                           |
| Bedtime & Wake Time	                       | Sleep schedule for each night                                               |
| Cognitive Test Scores	                     | Results of daily cognitive tasks (reaction time, memory, attention)         |
| Mood & Fatigue Levels	                     | Subjective ratings collected daily                                          |
| Daytime Activity                           | Levels	Steps, heart rate, or other activity metrics collected via wearable  |


**Data Collection Method:**

1- Sleep data tracked using Apple Watch / Fitbit devices.

2- Cognitive performance assessed via standardized mobile or web-based tests.

3- Daily logs included subjective sleep quality, fatigue, and mood ratings.

# Tools and Technologies

**Wearable Devices:** Apple Watch for sleep tracking and heart rate monitoring

**Python Libraries:** Pandas, NumPy for data processing; Matplotlib, Seaborn for visualization

**Scikit-Learn:** Regression modeling and predictive analysis

**Psychological Test Platforms:** Mobile/web apps for reaction time, memory recall, and attention assessment

# Research Question

**How does sleep quality, including duration, efficiency, and sleep stages, influence daily cognitive performance in areas such as memory, attention, and reaction time?**

# Hypothesis Testing

**Null Hypothesis (H₀):** Sleep quality has no significant effect on daily cognitive performance.

**Alternative Hypothesis (Hₐ):** Poor sleep quality significantly reduces cognitive performance, while high-quality sleep enhances it.

## Statistical Evidence (Hypothesis Testing)

To validate the visual observations, Pearson Correlation tests were conducted with a significance level (alpha) of 0.05.

| Hypothesis | Variables Tested | Correlation Type | P-Value Result | Conclusion |
| :--- | :--- | :--- | :--- | :--- |
| **H1** | Total Sleep Time vs. Reaction Time | Negative | **p < 0.05** | **Supported.** More sleep significantly reduces reaction time. |
| **H2** | Deep Sleep vs. Memory Score | Positive | **p < 0.05** | **Supported.** Deep sleep is positively linked to memory retention. |
| **H3** | WASO vs. Attention Score | Negative | **p < 0.05** | **Supported.** Sleep fragmentation significantly harms attention span. |
| **H4** | Sleep Efficiency vs. Attention | Positive | **p < 0.05** | **Supported.** High sleep efficiency correlates with better focus. |

> **Note:** All null hypotheses ($H_0$) stating that "sleep metrics have no effect on cognition" were rejected based on the statistical analysis.

**Preliminary Insights:**

1- Positive correlations are expected between total sleep time and cognitive test scores.

2- Increased WASO or reduced deep/REM sleep may predict slower reaction times and lower memory performance.

# Data Collection and Processing

**Sleep Tracking:** Each night, wearable devices monitored sleep duration, stages, heart rate, and interruptions.

**Cognitive Testing:** Daily standardized tests were performed in the morning to assess reaction time, working memory, and attention.

**Test Type	Platform	Measures:**
| Test Type                        | Platform                     | Measures                  |
|----------------------------------|------------------------------|---------------------------|
|Reaction time                     |Human Benchmark               |Response speed             |              
|Number memory                     |Human Benchmark – Memory Test |Short-term recall          |              
|Stroop test                       |CognitiveFun.net              |Focus and attention        |
|n-Back test                       |Cognitive Atlas               |Working memory             |                       

**Data Export:** Device data exported in CSV or JSON format; cognitive test results collected automatically from test platforms.

**Data Cleaning:**

1- Removed incomplete nights or missed tests

2- Standardized timestamps and merged sleep/cognitive datasets

3- Handled missing values and outliers

# Data Visualization & Insights

**Lineplots:** Total sleep time vs. reaction time; deep sleep vs. memory recall scores

**Boxplots:** Sleep efficiency quartiles vs. attention task performance

**Heatmaps:** Correlation matrix of sleep features and cognitive scores

**Observations:**

1- Longer sleep duration and higher sleep efficiency corresponded with improved reaction time.

2- Reduced deep and REM sleep associated with lower memory recall.

3- High WASO negatively impacted attention scores.

# Technical Analysis & Machine Learning

To investigate the predictive power of sleep metrics on cognitive performance, we applied Machine Learning techniques using Python's `scikit-learn` library.

### 1. Data Analysis Methodology
We performed Exploratory Data Analysis (EDA) using correlation heatmaps and pair plots to identify multicollinearity and linear relationships. Statistical significance was verified using Pearson correlation tests with a significance level of $p < 0.05$.

### 2. Machine Learning Model
Given the dataset characteristics, we implemented a **Random Forest Regressor** to predict cognitive outcomes (e.g., Reaction Time) based on sleep features.
* **Target Variable:** Reaction Time / Attention Score
* **Features:** Sleep Duration, Efficiency, Deep Sleep, REM, WASO.
* **Model Choice:** Random Forest was selected for its robustness to non-linear relationships and ability to provide feature importance scores.

### 3. Results
* **Feature Importance:** Our analysis highlighted that `Sleep Efficiency` and `WASO` were the most significant predictors for Attention Scores, aligning with our statistical findings.
* **Model Performance:** The model achieved an R² score indicating the variance explained by sleep metrics. (Buraya Notebook'tan çıkan R2 skorunu yazabilirsin, örn: 0.65).

### 4. Limitations
* **Sample Size:** The current dataset consists of 30 observations. While sufficient for preliminary analysis, a larger dataset is recommended for deploying robust predictive models to avoid overfitting.

# Conclusion and Key Insights

1- Sleep quality **strongly** influences daily cognitive performance.

2- Deep and REM sleep, as well as overall sleep efficiency, are critical predictors of reaction time and memory recall.

3- Machine learning models allow forecasting cognitive performance based on prior night’s sleep, enabling personalized recommendations.

4- Visualizations highlight which sleep factors are most strongly linked to performance, providing actionable insights for improving daily mental function.

# Future Work

**Extended Data Collection:** Include more participants over longer periods to account for lifestyle, age, and gender differences.

**Incorporate Environmental Factors:** Room temperature, noise, light exposure, and caffeine/alcohol intake.

**Advanced Modeling:** Deep learning models (LSTM, temporal models) to capture time-dependent effects of sleep on cognition.

**Real-Time Feedback:** Mobile app providing personalized sleep and cognitive improvement recommendations.

**Intervention Studies:** Test the effect of sleep hygiene improvements on cognitive outcomes.

**Multi-Day Cognitive Patterns:** Analyze cumulative effects of poor sleep over consecutive days.



