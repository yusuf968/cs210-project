The aim of this project is to analyze my step count data, which I obtained from my iPhone using the Health app. The dataset includes step count logs from August 2020 onward, along with additional information such as walking step lengths, walking speeds, and active energy burned. I performed a detailed analysis to identify patterns, correlations, and trends in my physical activity, and how different factors like time of day, walking speed, and step length impact energy expenditure.
I downloaded my step count data directly from the Health app, including step counts, timestamps, and metadata. I then performed the following preprocessing steps:
Data Formatting: Converted the raw data into a structured .xml format for easier processing.
Data Extraction: Used Pandas to extract and clean the relevant columns such as startDate, endDate, and value(step count).
Anonymization: Although the data was already anonymized, I ensured any identifiable metadata was removed.
Preprocessing: I derived additional metrics like walking distance (based on step length) and walking speed (based on time intervals) to provide a richer analysis.
Insights and Key Findings
Daily Trends: My activity levels fluctuate over time, with periods of high activity followed by inactivity (e.g., during holidays or busy work periods).
Walking Speed and Energy Burn: Faster walking speeds correlate with higher energy burn, confirming that walking speed is an important factor in calorie burning.
Step Length: Longer strides are more efficient, resulting in higher energy burn per step, suggesting that adjusting my walking technique could increase my efficiency.
Activity by Time of Day: I am most active in the afternoon, with significantly fewer steps taken during the night, which aligns with my sleep schedule.
Day of the Week Patterns: My activity is more consistent during the week, with Sundays being the exception due to personal commitments.

