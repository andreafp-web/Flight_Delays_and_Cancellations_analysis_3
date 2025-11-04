#  Flight Delay Analysis - Capstone Project

## Project Overview

This project explores flight delays and cancellations across the United States using a dataset of over 1 million flights from 2024. It combines Python-based data analysis, hypothesis testing, machine learning, and interactive dashboard design in Tableau to uncover patterns and predictive insights.

The goal is to help stakeholders — airlines, airports, and passengers — better understand delay behavior and improve operational planning.

---

## Dataset Content

The dataset was sourced from [Kaggle](https://www.kaggle.com/datasets/nalisha/flight-delay-and-cancellation-data-1-million-2024) and includes:

- Over 1 million flight records from 2024  
- Columns such as `fl_date`, `origin_city_name`, `dep_time`, `taxi_out`, `weather_delay`, `late_aircraft_delay`, and `distance`  
- Cleaned version includes an added `dep_hour` column for time-based analysis

### Cleaned Dataset

Due to GitHub’s file size limits, the cleaned flight dataset is hosted externally:

 [Download cleaned_flight_data.csv](https://drive.google.com/file/d/1kRC48SktgOd24EyuoVCt7eIev6QdcuhW/view?usp=sharing)

---

## Business Requirements

- Identify delay patterns by time, location, and flight characteristics  
- Understand how weather and operational factors influence delays  
- Predict taxi-out time using machine learning  
- Communicate insights to both technical and non-technical audiences

---

## Hypotheses & Validation

Ten hypotheses were tested, including:

1. Delays increase later in the day due to late-arriving aircraft ✅  
2. Weather delays are more frequent in winter months ✅  
3. Certain airports consistently show higher delays ✅  
4. Longer taxi-out times correlate with delays ✅  
5. Delays vary by weekday ✅  
6. High flight volume leads to longer delays ✅  
7. Long-distance flights experience fewer delays ✅  
8. Weather delays peak in January ✅  
9. Peak hours show higher taxi-out times ✅  
10. Major hub cities have longer delays ✅  

Each hypothesis was validated using grouped statistics, visualizations, and regression modeling.

---

## Project Plan

### Data Management
- Loaded and cleaned raw CSV in Python using `pandas`  
- Handled missing values, converted time formats, and added `dep_hour`  
- Exported cleaned dataset for Tableau

### Methodologies
- Exploratory Data Analysis (EDA)  
- Hypothesis Testing  
- Linear Regression (scikit-learn)  
- Visual storytelling with Seaborn, Matplotlib, and Plotly

### Mapping Visuals to Requirements
- Delay by Weekday → Scheduling inefficiencies  
- Delay Heatmap → Airport congestion  
- Taxi-Out vs. Delay Status → Operational bottlenecks  
- Distance vs. Delay → Flight planning insights

---

## Analysis Techniques

- Descriptive statistics: mean, median, standard deviation  
- Probability and distribution analysis  
- Regression modeling with `LinearRegression`  
- Visualizations with `matplotlib`, `seaborn`, and `plotly`

### Limitations & Alternatives
- No airline column → Used `origin` as proxy  
- Partial seasonal data → Limited weather analysis  
- Used boxplots and scatter plots to overcome lack of categorical features

---

## Generative AI Integration

- Used Copilot for:
  - Code optimization and debugging  
  - Dashboard layout planning  
  - Fixing code errors
  

---

## Ethics & Reflection Notebook

This project includes a dedicated notebook addressing ethical, legal, and reflective aspects of the analysis:

[View Ethics_Reflection_and_Project_Review.ipynb](./Ethics_Reflection_and_Project_Review.ipynb)

Topics covered:
- Bias and fairness in delay reporting  
- Legal and social implications of data use  
- Practical challenges and learning reflections  
- Development roadmap and continuous learning mindset

---

## 📊 Dashboard Design

### Flight Delay Dashboard Summary

This dashboard provides a comprehensive analysis of flight delays across the United States using 2024 flight data. It is organized into three key sections, each designed to explore different dimensions of delay patterns and their contributing factors.

 [View Dashboard on Tableau Public](https://public.tableau.com/app/profile/andrea.ferreira4559/viz/Flight_delays_analysis-Dashboard/Dashboard1)

#### 1. Delay Patterns
This section investigates how delays fluctuate based on time-related variables:

- **Late Aircraft by Hour**: Highlights peak hours for late aircraft delays, revealing operational bottlenecks.  
- **Weather Delay by Month**: Tracks seasonal trends in weather-related delays, identifying high-risk months.  
- **Delay Rate by Weekday**: Compares delay frequencies across weekdays to uncover scheduling inefficiencies.  

#### 2. Geographic Insights
This section focuses on spatial patterns in delay behavior:

- **Delay Heatmap by Airport and Hour**: Visualizes delay intensity across major airports and time slots.  
- **Average Departure Delay by Airport**: Ranks airports by average delay duration, highlighting performance gaps.  
- **Delay Rate by City**: Maps delay rates across cities to identify regional trends.  

#### 3. Distance & Taxi-Out Analysis
This section explores how flight distance and ground operations affect delays:

- **Taxi-Out Time by Delay Status**: Compares taxi-out durations for delayed vs. on-time flights.  
- **Taxi-Out Time by Distance Category**: Examines how flight length influences ground movement time.  
- **Delay Rate by Flight Distance**: Reveals how short-haul vs. long-haul flights differ in delay likelihood.  

#### Interactivity
To enhance user exploration, the dashboard includes filters tailored to each section:

- **Delay Patterns**: `weekday_name` — explore delay trends by day of the week  
- **Geographic Insights**: `origin_full_name` — focus on specific cities or airports  
- **Distance & Taxi-Out Analysis**: `distance_category` — compare short, medium, and long-haul flights  

---

### Unfixed Bugs & Challenges

#### Pandas Warning
Resolved using `.loc` and `.astype('Int64')` to ensure safe assignment.

#### Seaborn FutureWarning
> Note: Seaborn’s upcoming changes to `palette` without `hue` triggered a warning. Safe to ignore.

---

## Development Roadmap

### Challenges Faced
- Time formatting issues  
- GitHub file size limits  
- Missing airline column

### Next Steps
- Explore classification models  
- Add airline-level analysis  
- Enhance dashboard interactivity and publish additional insights

---

## Deployment

Dashboard is published to Tableau Public and accessible via the link above.

---

## Main Data Analysis Libraries

- `pandas` – data cleaning and manipulation  
- `matplotlib`, `seaborn`, `plotly` – visualizations  
- `scikit-learn` – regression modeling

---

## Credits

## Credits

This project was supported by a variety of tutorials, documentation, and community resources:

- [YouTube Tutorial: Tableau Dashboard Design](https://www.youtube.com/watch?v=6oFTdbrugUs)  
- [YouTube Tutorial: Linear Regression with Scikit-Learn](https://www.youtube.com/watch?v=ukZn2RJb7TU)   
- [CyberProof: AI & Data Security](https://www.cyberproof.com/blog/ai-data-security-key-threats-and-protection/)  
- [IEEE Digital Privacy Publications](https://digitalprivacy.ieee.org/publications)  
- LMS resources from Code Institute 
- Official documentation:
  - [Pandas](https://pandas.pydata.org/docs/)
  - [Seaborn](https://seaborn.pydata.org/)
  - [Scikit-learn](https://scikit-learn.org/stable/)
- Community support from Stack Overflow and Medium blogs  
- Dashboard layout inspired by public Tableau galleries  
- Microsoft Copilot for code support and documentation guidance


---

## Acknowledgements

Thanks to instructors, peers, and Microsoft Copilot for guidance and help resolving technical challenges throughout this project.


