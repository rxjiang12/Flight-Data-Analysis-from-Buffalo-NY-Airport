**Analysis of Flight Data from Buffalo Niagara International Airport (BUF)**

**Project Overview:**   
This project analyzes one month of flight activity at Buffalo Niagara International Airport (BUF) to better understand where delays and cancellations most frequently occur. By combining 30 days of raw flight data stored in JSON format, this analysis focuses on airline performance, destination trends, and how operational factors such as gates and scheduling contribute to delays.

The goal of this project was to organize and analyze flight operation data in order to identify patterns in departure and arrival delays, airline reliability, and potential areas for improving airport efficiency and the overall passenger experience.

**Project Objective:**   
The objective of this project was to analyze flight performance data from Buffalo Niagara International Airport (BUF) to identify patterns in departure and arrival delays across airlines, destinations, and operational factors.

**Business Problem:**   
Airports and airline operators must manage a wide range of operational challenges that can lead to delays or cancellations, such as:

* Scheduling Constraints  
* Gate Availability  
* Airline Performance  
* Weather Conditions  
* Flight Volume

Without structured analysis, it is difficult to determine where delays are concentrated or which operational factors contribute most to service interruptions. This project aims to provide data-driven insights into delay patterns at BUF Airport to support improved operational planning and performance monitoring.

**Dataset:**   
The dataset used in this analysis consists of 30 JSON files representing daily flight activity throughout January 2025 at Buffalo Niagara International Airport. Each file contains detailed information regarding:

* Scheduled and actual departure times  
* Scheduled and actual arrival times  
* Airline carrier information  
* Destination airports  
* Aircraft information  
* Gate assignments  
* Delay and cancellation indicators

These daily files were combined to create a unified dataset for analysis.

**Tools & Technologies:** 

* Python  
* Pandas  
* NumPy  
* Matplotlib

**Methodology:**   
The project followed a structured analytics workflow including:

1\. Data Preparation

* Loaded and combined 30 individual JSON flight data files into a single dataset  
* Cleaned raw flight records by handling missing values and inconsistent formatting  
* Standardized variables for scheduled and actual departure and arrival times  
* Calculated delay metrics such as departure delay and arrival delay  
* Prepared the dataset for aggregation and trend analysis

2\. Model Planning

* Identified key performance indicators related to flight delays  
* Selected relevant analytical dimensions including airline carrier, destination airport, gate assignment, and day of operation  
* Planned aggregation strategies to evaluate average departure delay, median departure delay, average arrival delay, and cancellation frequency

3\. Model Building & Analysis

* Performed exploratory data analysis using grouped aggregations  
* Analyzed delay trends by airline and destination  
* Evaluated operational bottlenecks across gates  
* Identified recurring delay patterns across specific dates and carriers  
* Generated summary statistics and visualizations to support findings

**Key Insights**

* Certain airlines and destinations consistently experienced higher average delays  
* Specific gates were associated with increased departure delays  
* Delay patterns varied by date, suggesting operational or scheduling pressures  
* A small number of destinations accounted for a disproportionate share of arrival delays

These findings highlight potential operational constraints and areas where targeted scheduling or resource allocation improvements may enhance performance at BUF Airport.

**How to Run This Project**

1. Clone or download this repository to your local machine.  
2. Ensure that Python is installed along with the required data analysis libraries, including Pandas, NumPy, and Matplotlib.  
3. Open the flight data notebook file in Jupyter Notebook or another compatible Python notebook environment.  
4. Run the cells sequentially to reproduce the data preparation, analysis, and visualization steps used in this project.

**Limitations**

* Analysis is limited to one month of flight data  
* External factors such as weather were not incorporated  
* Dataset does not capture airline staffing or maintenance issues

**Contributors**  
This was a collaborative academic project completed by:

* Anna Bold  
* Kossi Gamli  
* Ran Xin Jiang  
* Christina Pratas