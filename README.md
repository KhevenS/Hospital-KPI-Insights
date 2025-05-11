# Hospital KPI Dataset Analysis

## Project Overview
Using the raw datra gathered from states. Generate the KPIs after cleaning the raw state data. This project analyzes a hospital Key Performance Indicator (KPI) dataset focused on COVID-19 related metrics. The dataset includes information on ICU and inpatient bed utilization, age-based COVID-19 admissions, and data coverage metrics. The goal is to provide actionable insights for hospital resource management, patient care, and reporting quality.

## Tools Used
- **Python (Pandas, Matplotlib, Seaborn)**
- **Jupyter Notebook**
- Data source: U.S. HealthData.gov

## Dataset Summary
### Started with Raw dataset 
- **Rows:** 54
- **Columns:** 135 

### New dataset 
- **Rows:** 54
- **Columns:** 72
- **Focus:** COVID-19 hospital metrics (ICU, inpatient beds, admissions by age, coverage)
- **Missing Values:** None detected

## Key Objectives
- Monitor ICU and inpatient bed utilization rates
- Track COVID-19 specific bed usage
- Analyze admission trends by age group
- Evaluate data reporting coverage and quality

## Key Columns for Analysis
- `adult_icu_bed_utilization`
- `adult_icu_bed_covid_utilization`
- `inpatient_bed_covid_utilization`
- `previous_day_admission_adult_covid_confirmed_<age_group>`
- Coverage columns for each metric

## Tableau Dashboard Recommendations
- Create dashboards for capacity management, age-based analysis, and coverage monitoring
- Use filters and interactive elements for deeper insights
- Leverage calculated fields for utilization rates and trends

## Data Quality & Cleaning
- The dataset is clean and ready for analysis
- No missing values detected
- Consistent column naming conventions

## Getting Started
1. Load the dataset (`cleaned_hospital_kpi_dataset.csv`) into your analysis tool (e.g., Tableau, Python, Excel)
2. Use the key columns and objectives above to guide your dashboard or report creation
3. Refer to the suggested visualizations for inspiration

##  Visualizations

### ICU Bed Utilization Distribution
![image](https://github.com/user-attachments/assets/19a46caa-36d5-4d48-bebe-c569bc1a0c20)

#### **Interpretation:**

This comparison shows a shift in ICU burden:
- **General ICU demand remains high**, possibly due to other medical conditions or delayed procedures.
- **COVID-specific ICU strain is now minimal**, which could influence how hospitals allocate resources and plan future pandemic responses.
- adult_icu_bed_utilization has a higher and more spread-out distribution, with most facilities falling in the 60-80% range and some outliers at both ends. 
- adult_icu_bed_covid_utilization is much lower on average, with many values clustered near 0 and fewer high-utilization outliers. 
    - This suggested that NON-COVID paitents occupy a larger share of ICU beds at that date 

This type of distribution insight is valuable for both operational planning and public health evaluation.

![image](https://github.com/user-attachments/assets/d2c6012a-b474-45c6-80ca-e2f33cf51a77)

#### **Interpretation:**

- Each bar represents the mean number of daily admissions for a specific age group:
    - X-axis:Age groups (e.g., 18-19, 20-29,...,80+)
    - Y-axis:Average number of admissions 
- The height of each bar indicates how many people from that age group were admitted on average per day
- This trend highlights a **clear age-risk gradient**, where older adults are more likely to require hospitalization due to COVID-19.
- It supports public health strategies prioritizing older populations for preventive care, vaccination, and resource allocation.

This type of demographic insight is crucial for data-driven healthcare planning and age-targeted interventions.

### Correlation Between COVID-19 Admissions by Age Group
![image](https://github.com/user-attachments/assets/d4527fd2-92f8-4389-94d2-4f268cacdf3d)

This heatmap displays the Pearson correlation coefficients between COVID-19 hospital admissions for different adult age groups.

#### **Key Insights:**

1. **Strong Correlations Among Older Age Groups:**
   - Admissions for individuals aged **50–59**, **60–69**, **70–79**, and **80+** are highly correlated (correlation coefficients close to **0.90–1.00**).
   - This suggests that when admissions increase in one older group, they tend to rise across the others as well — likely due to shared risk factors, comorbidities, or exposure patterns.

2. **Weaker Correlation in Younger Age Groups:**
   - Age groups like **18–19** and **20–29** show much **lower correlations** with older cohorts (around **0.2–0.5**).
   - This reflects **distinct hospitalization trends** among younger adults, possibly influenced by different behaviors, immunity levels, or vaccination rates.

3. **Low Correlation for Unknown Categories:**
   - Groups labeled as `unknown_coverage` or `unknown_confirmed` show little to no correlation with any defined age group.
   - These likely represent incomplete or miscoded records and may require exclusion or separate handling in modeling tasks.

## Results Summary
- High ICU occupancy across most facilities
- Elderly populations (70–79, 80+) had the highest admissions
- Strong age-based correlation in hospitalization rates
- Dataset now clean and ready for dashboarding or modeling

## Repository Contents
| File | Description |
|------|-------------|
| `Hospital_Facilities_Capacity.ipynb` | Main notebook with data analysis |
| `cleaned_hospital_kpi_dataset.csv` | Final cleaned dataset |

## Author
**Khevendra Singh**  
Healthcare & BI Focus  
[LinkedIn](https://www.linkedin.com/in/khevendra-singh-a7054b305/) | [Portfolio](2)
