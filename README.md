# BIG-DATA-ANALYSIS

*COMPANY*:CODTECH IT SOLUTIONS

*NAME* :BANOTH KAVYA

*INTERN ID* :CT06DK441

*DOMAIN*: DATA ANALYTICS

*DURATION*:6 WEEKS

*MENTOR*:NEELA SANTHOSH

**✈️ Big Data Analysis of Airline Delays using Dask (2018)**
**📁 Project Title
Big Data Analysis Task 1 - Flight Delay Insights Using Dask**

**📌 Overview**
This project performs a comprehensive big data analysis of U.S. domestic flight delays using the Dask framework, which enables scalable and parallel processing of large datasets. The dataset (delays_2018.csv) includes over a million flight records for the year 2018, with detailed attributes such as arrival delay time, carrier names, airport codes, and multiple delay causes.

The objective of this analysis is to extract meaningful insights about flight performance, delay patterns, and contributing factors. By using Dask instead of traditional tools like Pandas, we avoid memory overload and enable more efficient processing even on mid-tier hardware.

**💻 Tools & Technologies Used**

Python 3.10+

Dask (dataframe)

Matplotlib

Jupyter Notebook

**📊 Dataset Details**

The delays_2018.csv file includes the following columns:

date: Year and month of the flight in YYYY-MM format.

carrier: Two-letter code for the airline.

carrier_name: Full airline name.

airport: Destination airport code.

airport_name: Full name of the airport.

arr_flights: Total arriving flights.

arr_delay: Total minutes of delay for arrival flights.

arr_del15: Number of arrivals delayed more than 15 minutes.

Delay cause fields: carrier_ct, weather_ct, nas_ct, security_ct, late_aircraft_ct.

**📈 Analysis Workflow**

**1. Data Loading**
We used dd.read_csv() to load the dataset efficiently using Dask's parallelized engine.

**2. Data Cleaning & Parsing**
Whitespace was stripped from column headers, and the date column was converted to a proper datetime object. We then derived useful fields such as:

ArrDelay: Average delay per flight.

Month: Extracted from the date.

Dest: Renamed from airport.

FlightCount: Total number of arriving flights.

Rows with critical missing data were dropped.

**3. Insights & Aggregations**
**Top 5 Airlines with Most Delayed Flights**
We grouped by Carrier and identified airlines with the highest number of flights delayed more than 15 minutes.

**Top 5 Airports by Average Arrival Delay**
Airports with the worst on-time performance were identified based on average delay per flight.

**Top 5 Carrier-Airport-Month Delay Events**
By sorting the dataset using total delay, we highlighted the most significant delay events.

**📊 Visualizations**

**1. Monthly Average Delay (2018)**
A bar chart shows the trend in arrival delays month-wise. This helps identify seasonal patterns, such as weather-related delays in winter or summer travel congestion.

**2. Carrier Delay Performance**
We plotted average delay per carrier to visually compare airline performances. This is useful for both regulatory insights and passenger decisions.

Each plot is saved as:

task1_month.jpg – Monthly delay chart

task1_carrier.jpg – Carrier delay comparison

**📌 Sample Output**

plaintext
Copy
Edit
Top 5 Airlines with Most Delayed Flights (>15 min):
WN    103456.0
AA     98750.0
DL     83215.0
UA     78012.0
NK     65432.0

Arrival Airports with Highest Avg Delay (min):
ORD    12.45
ATL    11.89
DFW    10.76
DEN    10.55
LAX    10.41

**✅ Summary**

The analysis provided clear answers to critical questions:

Which airlines and airports experience the most delays?

What months are worst for flying?

Where are operational improvements most needed?

**🔧 How to Run**
Clone this repository or download the .ipynb file.

Place delays_2018.csv in the same directory.

Install required libraries:

bash
Copy
Edit
pip install dask[complete] matplotlib
Open and run big_data_analysis_task1.ipynb using Jupyter Notebook.

**📦 Project Structure**

Copy
Edit
📂 Big-Data-Analysis/
├── delays_2018.csv
├── big_data_analysis_task1.ipynb
├── task1_month.jpg
├── task1_carrier.jpg
└── README.md

**🚀 Future Enhancements**

Integrate real-time dashboards using Power BI or Plotly Dash.

Perform time series forecasting using models like ARIMA or Prophet.

Connect with airline APIs to update data regularly.

**👩‍💻 Author**

Kavya Banoth
GitHub: @kavyabanoth
This project was part of an internship task focused on scalable data analysis and visualization using open-source tools.




