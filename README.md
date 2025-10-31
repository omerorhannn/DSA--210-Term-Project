# The Impact of Sleep Quality on Daily Cognitive Performance
# Motivation

This project aims to analyze how sleep quality and duration affect daily cognitive performance, measured through focus-related metrics such as screen time, typing accuracy, and reaction time.

Using Apple Watch and phone usage data, I will examine how variations in total sleep time, heart rate variability (HRV), and sleep stages (deep vs. light sleep) influence mental efficiency indicators — like productivity duration, error rate in short cognitive tests, and attention levels.

The goal is to quantify how sleep consistency translates into measurable cognitive output, bridging the gap between physiological recovery and everyday performance.

# Objectives

Track Sleep Metrics:
Collect daily sleep data (total sleep time, REM percentage, HRV, average heart rate) using Apple Watch and Health App data.

Measure Cognitive Performance:
Record numerical indicators of focus — such as screen-time-based productivity, phone unlock frequency, or simple reaction-time test scores from a mobile app.

Analyze the Relationship:
Apply correlation and regression analyses to explore how variations in sleep metrics impact focus and performance outcomes.

Develop Predictive Insights:
Build a simple machine learning model that predicts focus/performance level from prior-night sleep data, supporting better rest-planning strategies.

# Dataset
Variable	Type	Description
Total Sleep Duration (hours)	Numerical	Total time asleep per night
REM Sleep (% of total)	Numerical	Percentage of deep REM sleep
Heart Rate Variability (ms)	Numerical	Average HRV during sleep (indicator of recovery)
Average Resting Heart Rate (bpm)	Numerical	Nighttime average HR
Sleep Efficiency (%)	Numerical	Ratio of time asleep vs. in bed
Cognitive Test Score (0–100)	Numerical	Daily short reaction-time or focus test result
Phone Screen Time (minutes)	Numerical	Proxy for daily focus or fatigue
Focus Level (binary)	Categorical	1 = High-focus day, 0 = Low-focus day (derived)
⚙️ Tools and Technologies

Apple Watch / Health App: Sleep tracking (duration, HRV, heart rate, REM).

Python (NumPy & Pandas): Data processing and statistical analysis.

Matplotlib & Seaborn: Correlation heatmaps, time-series plots, and boxplots.

Scikit-Learn: Regression & classification modeling (e.g., Logistic Regression, Random Forest).

Jupyter Notebook: Code development and visualization.

# Research Question

How does sleep quality — measured by total duration, HRV, and REM percentage — influence daily cognitive performance and focus levels?

# Hypothesis Testing

H₀ (Null Hypothesis): Sleep quality (duration, HRV, REM %) has no significant effect on cognitive performance.

Hₐ (Alternative Hypothesis): Higher sleep quality and longer duration significantly improve cognitive performance.

Tests to use:

Pearson & Spearman correlations

t-tests between “high-focus” vs. “low-focus” days

Linear regression predicting performance from sleep metrics

# Data Collection and Processing

Data Acquisition via Apple Health Export

Collect 30 days of sleep records from the Health app.

Variables: total sleep time, REM %, HRV, resting heart rate.

Daily Cognitive Tests

Use a simple reaction-time or focus app (e.g., Stroop test or typing-speed test) each morning.

Record results (accuracy, response time, or score / 100).

Data Integration

Export both datasets (.xml → .csv).

Parse XML using Python (xml.etree.ElementTree, pandas).

Merge by date (sleep → next-day performance).

Data Cleaning

Handle missing values (forward-fill).

Remove days with incomplete measurements.

Add derived variables:

Sleep efficiency = (actual sleep / time in bed) × 100

Focus level = 1 if performance ≥ median else 0

# Data Visualization and Analysis

Line plots: Sleep duration vs. performance score over 30 days.

Heatmap: Correlations between HRV, REM %, screen time, and focus.

Boxplots: Performance grouped by “short” (< 6 h) vs. “long” (> 7 h) sleep.

Scatterplot: HRV vs. reaction-time performance.

# Machine Learning Objective

A lightweight predictive model to estimate the probability of a high-focus day based on previous-night sleep data.

Features:
Total Sleep, REM %, HRV, Resting HR, Sleep Efficiency
Target: Focus Level (0/1)

Models:

Logistic Regression (baseline)

Random Forest Classifier (non-linear)

Metrics: Accuracy, Precision, Recall, F1-score

# Expected Results

Positive correlation between total sleep and focus score.

Higher HRV → better reaction-time performance.

Random Forest achieves highest predictive accuracy (~70–80 %).

# Conclusion

This project demonstrates how physiological recovery (sleep metrics) affects cognitive output and focus.
It merges numerical (sleep data) and behavioral (focus test / screen-time data) sources to reveal actionable insights about recovery and productivity.
The findings can inform personalized sleep optimization strategies for students, athletes, or professionals.

# Future Work

Extend the dataset to multiple months for stronger statistical power.

Include subjective self-ratings of fatigue or motivation.

Apply time-series models (ARIMAX / LSTM) to forecast focus trends.
