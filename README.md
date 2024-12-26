Motivation

I’ve always been curious about how my daily habits influence my step count and overall physical health. Since I use my iPhone to track this data through the Health app, I saw an opportunity to explore:

How my activities change throughout the day and week.
The relationship between walking speed, step length, and energy expenditure.
The impact of lifestyle changes (e.g., holidays, busy work periods) on my step count.
By conducting this analysis, I hope to make data-driven improvements to my daily routine and better understand my exercise habits.

Tools

Jupyter Notebook: Used for coding, exploratory data analysis (EDA), and documentation.
Pandas: For data cleaning, filtering, and structuring.
NumPy: For handling numerical operations.
Matplotlib & Seaborn: For data visualization and plotting.

Data Source

My data primarily comes from the iPhone Health app. Apple allows users to export their health data in an XML format. Specifically, I used:

Health App Export
Contains step counts, timestamps, walking distances, walking speeds, active energy, and more.

Data Export Process:

Open Health App on iPhone, go to profile > Export All Health Data.
The app generates a ZIP file containing a large XML file of personal health records.
This XML file was then converted into a structured CSV using Python scripts.

Data Processing

I performed several preprocessing steps to transform raw data into clean, usable formats:

XML to CSV Conversion
Used Python to parse the XML file and export relevant fields (e.g., startDate, endDate, value for step counts) into CSV.
Data Cleaning
Dropped any rows with missing or invalid values.
Converted timestamps to a consistent time zone and extracted day-of-week and hour-of-day columns.
Anonymization
Removed or masked any sensitive metadata (e.g., Apple Watch device IDs) to ensure privacy.
Feature Engineering
Walking Distance: Derived from step count and average step length.
Walking Speed: Computed by dividing distance by time intervals.
Energy Expenditure: Linked active energy burns with step count data.
Time-based Features: Such as morning, afternoon, evening, and night categories.

Data Visualizations

All visual explorations are available in the data_visualization.ipynb notebook. Key plots include:

Daily Step Count: Line plots or bar charts showing how step counts vary by day.
Hourly Distribution: Heatmaps or histograms that visualize when during the day I tend to be most active.
Walking Speed vs. Energy Burn: Scatter plots examining the relationship between speed and energy expenditure.
Correlation Matrices: Highlighting correlations between variables (e.g., step length, walking speed, energy burn).
If you are viewing this on GitHub, please note that interactive Altair charts may not render correctly. Static images are provided in the figures folder for reference.

Data Analysis

Daily Trends
One of the first analyses was understanding how my step counts vary day-by-day. Notable observations include spikes during workdays versus weekends, as well as dips during holidays or travel periods.

Walking Speed and Energy Burn
Faster walking speeds show a positive correlation with higher energy burn. This suggests that intensity plays a key role in total calorie expenditure.

Step Length Efficiency
Longer strides appear to correlate with a higher energy burn per step. This finding suggests that adjusting my walking technique could potentially increase walking efficiency.

Activity by Time of Day
Most of my activity occurs in the afternoon, with minimal step counts late at night—likely reflecting normal sleep routines. This time-based analysis helps identify when I’m most active and when I might incorporate more exercise.

Day of the Week Patterns
Weekdays tend to have more consistent step counts, whereas Sundays (and sometimes Saturdays) show variable activity patterns due to personal commitments or leisure activities.

Findings

Daily Inconsistencies: My step count is not uniform; there are distinct periods of high/low activity.
Faster Walking = Higher Calorie Burn: Speed is a key factor in overall energy expenditure.
Longer Strides: They seem more efficient, yielding more calories burned per step.
Afternoon Peaks: Peak activity generally occurs in the afternoon, aligning with typical work/life schedules.
Weekend Variability: Sundays often differ from weekdays due to non-work-related commitments.

Limitations

Data-Sourced Limitations
Export Format: The Apple Health export may exclude certain metadata or workout details not tracked by the Health app.
Device Reliance: Data is only as accurate as the phone’s (or watch’s) motion sensors; periods without the device are not recorded.
Personal Limitations
Privacy: Some sensitive information (e.g., location, specific health metrics) was removed or masked, limiting deeper analysis.
Analysis Scope: The analysis was done over a certain period, so any long-term trends outside this window are not captured.
Knowledge Gaps: As I am continuously learning data science techniques, there may be advanced methods yet to be applied.
