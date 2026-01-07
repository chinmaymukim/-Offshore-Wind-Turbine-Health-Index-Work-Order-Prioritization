# -Offshore-Wind-Turbine-Health-Index-Work-Order-Prioritization
A data-driven asset health monitoring and maintenance prioritization framework combining SCADA sensor intelligence with CMMS work order analytics for offshore wind turbines.

🚀 Project Overview

Offshore wind farms operate in harsh, high-cost environments where unplanned failures can lead to massive production losses and safety risks.
This project introduces a comprehensive, dynamic Health Index framework that:

Continuously evaluates wind turbine health

Detects early warning signs from SCADA data

Quantifies maintenance risk using work order history

Enables data-driven prioritization of maintenance actions

📌 Outcome:
A single, interpretable Health Index score (0–100) per turbine that supports predictive maintenance, risk-based inspections, and smarter resource allocation.

🧠 Key Objectives

✔ Combine real-time SCADA sensor anomalies with historical maintenance data
✔ Identify high-risk turbines before failure occurs
✔ Prioritize critical work orders using a multi-factor risk model
✔ Quantify maintenance impact and risk reduction
✔ Provide clear visual insights for decision-makers

📊 Data Sources
1️⃣ SCADA Data (Operational Health)

Timestamped turbine-level sensor readings

Metrics used:

Gearbox temperature

Nacelle temperature

Hydraulic pressure

Cooling pressure

2️⃣ CMMS / SAP Work Orders

793 maintenance work orders

Attributes:

Priority & urgency

Planned costs

Lead time

Recurring issues

Turbine location & description

🔧 Methodology & Pipeline
🔹 Step 1: Exploratory Data Analysis (EDA)

Missing value checks

Outlier detection using boxplots

Correlation analysis

Data consistency validation

📌 Result: Clean, reliable datasets ready for risk modeling

🔹 Step 2: SCADA Risk Scoring (Anomaly-Based)

Threshold-driven anomaly detection applied to each sensor:

Sensor	Threshold
Gearbox Temperature	> 75°C
Nacelle Temperature	> 60°C
Hydraulic Pressure	> 250 bar
Cooling Pressure	> 200 bar

For each turbine:

Count of threshold breaches

Aggregated anomaly score

Normalized to 0–100 SCADA Risk Score

📌 Insight:
Turbines with persistent sensor excursions are flagged as high operational risk

🔹 Step 3: Work Order Risk Scoring (CMMS Intelligence)

A multi-dimensional WO risk model incorporating:

Priority & urgency

Planned maintenance cost

Lead time (start → finish)

Recurring failure patterns

Failure frequency

Normalized WO Risk Score (0–100) per turbine enables:

Objective maintenance prioritization

Identification of chronic problem turbines

📌 Key Improvement:
Moves beyond simple WO counts → true operational risk quantification

🔹 Step 4: Health Index Calculation

A unified turbine Health Index is computed using weighted fusion:

Health Index = w₁ × SCADA Risk + w₂ × Work Order Risk


📌 Multiple weighting strategies tested:

50 / 50

60 / 40 (SCADA dominant)

Sensitivity analysis performed to validate robustness

📈 Results & Key Insights
🔺 Top 10 Most At-Risk Turbines

Identified turbines with high anomaly frequency and heavy maintenance burden

Enables proactive inspections and failure prevention

🟢 Healthiest Turbines

Low anomaly counts

Minimal maintenance intervention required

Supports optimized resource allocation

📉 Maintenance Impact Analysis

Simulated resolution of top 3 highest-risk work orders:

Metric	Before	After
Average WO Risk Score	0.6531	0.6482

📌 Demonstrates measurable system-wide risk reduction

📊 Visual Analytics Delivered

Turbine Health Index bar charts

SCADA vs WO risk scatter plots

Heatmaps of anomaly concentration

Risk sensitivity analysis plots

Distribution of health scores across the fleet

📌 Designed for engineers, asset managers, and leadership

🧪 Sensitivity & Robustness Testing

Tested multiple SCADA/WO weight combinations

Health Index remains stable and interpretable

Confirms model reliability under different assumptions

🛠️ Technologies Used

Python

Pandas & NumPy

Matplotlib & Seaborn

Jupyter Notebook

Excel-based SCADA & SAP CMMS data

⚠️ Assumptions & Limitations

Fixed sensor thresholds (can be enhanced using ML)

Equal failure severity assumption (extendable)

WO text not yet NLP-processed (future scope)

🔮 Future Enhancements

🚀 Machine learning–based anomaly detection
🚀 NLP classification of work order descriptions
🚀 Time-decay health index (dynamic scoring)
🚀 Integration with vibration & alarm logs
🚀 Live dashboard (Power BI / Streamlit)

💡 Business Value

✔ Enables predictive maintenance
✔ Reduces unplanned downtime
✔ Improves maintenance efficiency & safety
✔ Supports data-driven asset management decisions
