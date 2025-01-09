
# Health Data Analysis Project

You can find the report on the project folder as pdf.

Project Hypothesis:

Faster or more frequent walking (i.e., higher step counts and speeds) will be associated with greater overall energy expenditure (kcal).

Objective:

I’ve long been interested in how my daily habits influence my step count and overall physical health. Leveraging my iPhone’s Health app data, this project explores:

How activity patterns vary by day of the week, season, and time of day.
Relationships between step length, steps per kilometer, distance, and active energy burn.
How lifestyle changes (e.g., holidays, busy work periods) affect my overall activity levels.
By analyzing these factors, I aim to make data-driven improvements to my daily routines and gain deeper insights into my walking/exercise habits.

Tools:

Jupyter Notebook: Primary environment for data cleaning, exploratory data analysis (EDA), and documentation.
Pandas: Data wrangling, aggregation, and feature engineering.
NumPy: Numerical computations.
Matplotlib & Seaborn: Visualization of trends, correlations, and distributions.

Data Source:

Apple Health Data

My data is sourced from the iPhone Health app export:

Health App Export: Contains records of step counts, distance walking/running, walking step length, active energy burned, etc.

Data Export Process:

In the Health app on iPhone, navigate to profile > Export All Health Data.
A ZIP file is generated containing an XML file of health records.
This XML was parsed and converted into CSV files using Python scripts for more convenient analysis.

Data Processing:

XML to CSV Conversion

Python scripts extracted the relevant fields (e.g., startDate, endDate, value) and wrote them into separate CSV files (Steps, Distance, Energy, etc.).

Removed rows with missing or invalid values.
Converted timestamps to datetime objects in local time.
Created additional columns like day-of-week, month, and season for easy grouping.

Merging:

Combined daily data into a single DataFrame, resulting in key columns such as total_steps, total_distance_km, total_kcal, and avg_step_length_cm.
Derived additional metrics:

steps_per_km: Steps / Distance

kcal_per_step: Calories / Steps

kcal_per_km: Calories / Distance

All EDA can be found in the Jupyter notebooks within this repository. Some key analyses include:

Daily, Monthly, and Seasonal Trends

Daily Aggregation: Summed or averaged metrics per calendar day (e.g., total steps, total distance).

Monthly & Seasonal Aggregations: Observed how these metrics change over months or across seasons (Winter, Spring, Summer, Autumn).

Correlation Analysis

Computed correlation matrices to see how avg_step_length_cm, steps_per_km, total_kcal, and other metrics relate.

Created heatmaps and scatter plots (with optional regression lines) to visualize relationships.
Time-of-Week & Time-of-Day Patterns

Analyzed activity by weekday (e.g., Monday vs. Sunday) to detect workweek vs. weekend trends.

Explored whether step count peaks occur in the morning, afternoon, or evening.

Pairwise Comparisons

Generated pair plots of key variables (total_steps, total_distance_km, total_kcal, avg_step_length_cm, etc.) to identify outliers or interesting clusters.

Key Findings:

Daily Inconsistencies

Step counts varied noticeably day-to-day, revealing spikes on some weekdays and dips during holidays or busy work periods.

Step Length & Efficiency

An inverse correlation was observed between avg_step_length_cm and steps_per_km (fewer steps needed per km when taking longer strides).

Longer strides often accompanied higher energy burn per step, implying that stride length can influence walking efficiency.

Walking Speed & Energy Burn

Higher walking speeds tended to correlate with greater total energy burn, suggesting that walking intensity is a significant factor in calorie expenditure.

Activity by Time of Week

Weekdays: More consistent step patterns.

Weekends: Sundays occasionally showed significant drops or spikes, likely reflecting leisure activities or rest days.

Seasonal Trends

Warmer months (Spring/Summer) appeared to have higher overall distances and step counts.
Winters often showed dips, possibly due to inclement weather or reduced daylight.

Limitations:

Device & Data Constraints

The Apple Health export may omit certain metadata or specific workouts.
Periods without carrying the phone remain untracked.
