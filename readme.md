# GB Heat Pump Data Analysis

This repository contains an end-to-end workflow for analysing **domestic heat pump electricity consumption in Great Britain**, based on the *Electrification of Heat (EoH)* study. The analysis develops **daily load-shape profiles, seasonal segmentation, and clustering** to identify representative usage patterns and their variability.  

This project complements my related work on the **NIE Smart Meter Trial**, enabling structured GB–NI comparisons of residential heat pump demand.

---

## Objectives

- Construct **seasonal weekday and weekend profiles** of heat pump demand.  
- Apply **K-Means clustering** with **silhouette analysis and the elbow method (WCSS)** to identify typical daily usage patterns.  
- Assess **hourly variability** of clusters using boxplots.  
- Provide a reproducible pipeline while ensuring **confidential raw data is not shared**.

---

## Methods (Summary)

1. **Data Preprocessing**  
   - Resampled half-hourly data into **hourly demand profiles**.  
   - Applied completeness checks (e.g., ≥90% daily coverage) and handled missing values.  
   - Split dataset into **winter vs summer** and **weekday vs weekend** subsets.  

2. **Normalisation**  
   - Applied **shape-based normalisation** (z-score or scaling to daily mean) to highlight usage *patterns* over absolute magnitude.  

3. **Clustering**  
   - Ran K-Means clustering for multiple \(k\) values (e.g., 2–10).  
   - Selected optimal cluster count using:  
     - **Elbow method (WCSS)** for compactness.  
     - **Silhouette score** for separation.  

4. **Visualisation & Results**  
   - Produced **median daily profiles** per cluster.  
   - Generated **hourly boxplots** to capture variability within clusters.  
   - Summarised cluster metrics and relative shares of households/days.

## Results
  - **Clustered profiles**: Representative shapes of heat pump demand across households.  
  - **Seasonal variation**: Winter profiles show pronounced evening peaks, while summer usage is flatter and dominated by hot water demand.  
  - **Hourly variability**: Boxplots highlight the spread of demand across clusters, capturing behavioural and technical heterogeneity.

## Data Availability
  The dataset originates from the **BEIS Electrification of Heat (EoH) study** and is subject to confidentiality restrictions.  
  Therefore, **raw data is not included** in this repository.  

  This repository provides instead:  
    - **Analysis code** (Jupyter notebooks and Python scripts).  
    - **Illustrative outputs** (figures and tables in `results/`).  
    - **Documentation of methodology** for reproducibility.  

  Researchers with legitimate access to the EoH dataset can reproduce the results by pointing the workflow to their local copy of the data.


## Contact

   Rahul Sajith Pillai
   
   PhD Researcher - Ulster University, Belfast
   
   Email: pillai-rs@ulster.ac.uk

   [LinkedIn](https://www.linkedin.com/in/rahul-sajith-p-02a7b6a3)
   

