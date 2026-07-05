# Zomato Kitchen Preparation Time (KPT) Optimization
Data Engineering | ETL | Feature Engineering | Business Analytics | Python
The objective was to improve Zomato's Kitchen Preparation Time (KPT) prediction by identifying unreliable merchant-generated signals and designing an ETL pipeline that generates more reliable features before data reaches the prediction model.
Instead of retraining the machine learning model, the project focuses on improving data quality through feature engineering and signal enrichment.

# WORKFLOW
Merchant Data

↓

GPS Signals

↓

POS Data

↓

Acoustic Signals

↓

Geofence Data

↓

ETL Pipeline

↓

Trust Score

↓

Chaos Index

↓

Adjusted KPT

↓

ETA Prediction

# DATASET
Since production data was unavailable during the hackathon, a synthetic dataset containing approximately 3,000 restaurant orders was generated.
The dataset simulated:

• Merchant bias

• Kitchen rush hours

• Rider arrival

• POS tickets

• Acoustic noise

• Different restaurant tiers

# FEATURE ENGINEERING
### Trust Score
Measures merchant reliability by comparing manual food-ready timestamps with rider GPS departure.

Higher gap → Lower Trust Score

### Chaos Index

Estimates kitchen workload using:

- POS tickets
- Acoustic noise
- Geospatial footfall
Higher workload → Higher estimated preparation time

### Adjusted KPT
Combines merchant input with Trust Score and Chaos Index to generate a more reliable preparation time.

## Expected Business Impact

Reduced Rider Waiting Time
Improved ETA Accuracy
Better Customer Experience
Reduced Manual Bias
Improved Dispatch Efficiency
Scalable ETL Architecture

