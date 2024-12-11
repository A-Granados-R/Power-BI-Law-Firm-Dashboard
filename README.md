# Power-BI-Law-Firm-Dashboard

## Table of Contents 

- [Project Overview](project_overview)
- [Data Sources](data_sources)
- [Tools](tools)
- [Data Cleaning](data_cleaning/preparation)
- [Exploratory Data Analysis](Exploratory_Data_Analysis)
- [Data Analysis](data_analysis)
- [Results/Findings](Results/Findings)
- [Recommendations](Recommendations)
- [References](References)

### Project Overview 

The goal of this dashboard is to introduce a Law Firm to Data Visualization. They didn't track nor analyse data before. This Dashboard was part of a presentation on what information we needed to track in order to get the most useful data so they could start taking data driven decisions.   

## Data Sources 

- Matters open: XSL file exported from their case management system 'Practice Panther' cointaining the count of cases open 
- New Leads: Exported XLS from their lead management software 'Lawmatics' cointaining detailed information of incoming leads 
- Sets: File exported from 'Lawmatics' cointaining appointment's information 
- Hires: File cointaining all the information from converted leads to hires, from 'Lawmatics'

### Tools 

- Excel - Data Cleaning (Not able to share since it cointains important information)
- Power BI - Create Reports & Visuals
- Statistics (DAX) - Percentage Calculation

### Data Cleaning/Preparation

In the initial data preparation phase, I perfomed: 
1. Data loading and inspection
2. Handled missing and duplicated values
3. Data cleaning and formatting

### Exploratory Data Analysis 

EDA involved exploring the leads data to answer: 

- Leads, appointments, hires on X amount of time
- Which marketing source is performing better?
- What are the conversion %?

### Data Analysis

Inside Power BI under model view I created relationships between forgein key "matter_id" for (new_matter, appointments and hires)tables  which made the DB interactive 
I also added the following formulas to get the conversion percentage 

```DAX
Sets scheduled = DIVIDE(SUM(appointments[matter_id]), SUM(new_matters[matter_]))
```

### Results/Findings 

1. Stakeholders received the visual data they were looking for a long time
2. Google and referals are the firm's best performing sources
3. They convert 41% leads to opportunities and 16% to hires

### Recommendations 

Based on the analysis, I recommended the following 
- Implement new workflows to track estimated case/lead value
- Track the time a lead spends in each stage of the pipeline to identify bottlenecks
- Investing in Google as our primary marketing source 

### References 

1. Chat GPT-4
3. [Microsoft Learning](https://learn.microsoft.com/es-es/training/modules/get-started-with-power-bi/)
