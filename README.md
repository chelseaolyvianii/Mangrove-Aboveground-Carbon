# Mangrove Aboveground Carbon (AGC) Estimation & Feature Ablation Study
This repository contains the code and methodology for evaluating the relative contributions of optical (Sentinel-2) and structural (GEDI LiDAR) features in predicting Aboveground Carbon (AGC) in the mangrove ecosystems of Rinca Island, Indonesia.
Using XGBoost regression and an ablation study framework, this project investigates whether optical spectral and textural data can effectively substitute vertical LiDAR metrics for mangrove carbon monitoring.

# Key Highlights & Results
- Dataset Size: 10,139 sample points with AGC values ranging from 0.04 to 251.56 Mg C/ha (Mean: 15.24 Mg C/ha).
- Optimal Feature Set: Combining horizontal spatial textures (GLCM) with vertical structural canopy profiles (LiDAR) yielded the highest accuracy.
- Best Model Performance: R^2 = 0.8779, RMSE = 6.6687 Mg C/ha (GLCM + LiDAR).
- Core Finding: Optical data alone suffers from spectral saturation in high-density mangrove canopies. While GLCM textures significantly improve optical predictions over raw bands/indices, GEDI LiDAR structural features (specifically RH95) remain indispensable for accurate AGC estimation.

# Tech Stack & Methods
Machine Learning: XGBoost (XGBRegressor), Scikit-Learn (KFold Cross-Validation, GridSearchCV)
Data Analysis & GIS: Pandas, NumPy, GeoPandasData Visualization: Matplotlib, SeabornEvaluation Metrics: Coefficient of Determination (R^2), Root Mean Squared Error (RMSE), Mean Absolute Error (MAE)

# Citation & References
Study Area: Rinca Island, Komodo National Park, NTT, Indonesia.
Data Sources: GEE (Sentinel-2) and GEDI Satellite (LiDAR)