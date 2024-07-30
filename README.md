# Road-Accident-Analysis-Power-BI

The purpose of this Power BI dashboard is to analyze road accident data and identify patterns and trends that can help improve road safety. The data includes information about accidents, such as the number of vehicles involved, severity of the accident, and the location and time of the accident.

The report aims to explore series of visualizations that will help us to better understand the data, and gain insights into patterns and trends related to the data. 

Analyzing accident data is paramount for enhancing safety measures and staying proactive. By delving into accident patterns, experts can craft targeted solutions to prevent future incidents. This data is instrumental in optimizing traffic management, designing safer roads, and making efficient resource allocations. Through insightful analysis, we can detect emerging trends, take prompt action, and consistently enhance safety protocols. Ultimately, it's about leveraging data to save lives and cultivate a safer transportation network for all.

## Analysis based on 

   . Total Casualties and Total Accident values for Current Year(CY) and YoY growth

   . Total Casualties by Accident Severity for Current Year and YoY growth

   . Total Casualties with respect to vehicle type for Current Year

   . Monthly trend showing comparison of casualties for Current Year and Previous Year (PY)

   . Casualties by Road Type for Current year

   . Current Year Casualties by Area/ Location & by Day/ Night

   . Total Casualties and Total Accidents by Location.

   . Total Accident values and Road Type for Current Year(CY). 

   . Total Accident by Local Authority(District) for Current Year.

   . Total Accident with respect to Speed limit for Current Year.

   . Total Accident with respect to Days of Week for Current Year.

   . Total Accident by Junction detail for Current Year.

   . Total Accident and Road Surface Conditions for Current Year.

   . Total Casualties and Total Accidents by Police Force for Current Year.


Cards-Accident Severity by Casualties Analysis(Total Current Year Casualties, Total Current Year Accidents, Current Year Casualties Fatal, 

Current Year Casualties Serious, Current Year Casualties Slight).

Multi-row Card-Number of Casualties by vehicle type.

Area Chart-Current Year Casualties vs Previous Year Casualties Monthly Trend, Number of accident by road surface.

Clustered bar Chart-Number of casualties by road type, Number of accident by district.

Stacked column chart-Police force in accident and casualties.

Pie Chart-Number of casualties by Urban/Rural.

Donut Chart-Number of casualties by Light Condition, Number of accident by junction.

Ribbon chart-Number of accident by road type.

Funnel-Number of accident by speed limit.

Treemap-Number of accident by days of week.

Map-Number of casualties by Location.

Slicers-Road Surface, Weather Conditions.


## Data Analysis Expressions (DAX) Formulas Used in Measures

### Total Casualties For Current Year and Year on Year Growth

(a) Current Year To Date Casualties -- CY Casualties Measure

CY Casualties = TOTALYTD(SUM(Data[Number_of_Casualties]), 'Calendar'[Date])

(b) Previous Year Casualties -- PY Casualties Measure

PY Casualties = CALCULATE(SUM(Data[Number_of_Casualties]), SAMEPERIODLASTYEAR('Calendar'[Date]))

(c) Year on Year Growth of Casualties - YoY Casualties Measure

YoY Casualties = ([CY Casualties] - [PY Casualties])/[PY Casualties]

### Total Accidents for Current Year and Year on Year Growth

(a) Current Year Accidents Count -- CY Accidents Count Measure

CY Accidents Count = TOTALYTD(COUNT(Data[Accident_Index]), 'Calendar'[Date])

(b) Previous Year Accidents Count -- PY Accidents Count Measure

PY Accidents Count = CALCULATE(COUNT(Data[Accident_Index]), SAMEPERIODLASTYEAR('Calendar'[Date]))

(c) Year on Year Growth of Accidents - YoY Accidents Measure

YoY Accidents = ([CY Accidents Count]-[PY Accidents Count])/[PY Accidents Count]




