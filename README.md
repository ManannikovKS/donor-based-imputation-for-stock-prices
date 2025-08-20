# Donor-Based Imputation for Stock Prices

This project develops a machine learning method to impute missing values in adjusted close prices.  
Compared to simple linear interpolation, the approach reduces error by ~25%.

---

## Method

- **Donors:** related assets, linearly interpolated and converted to log returns.  
- **Target:** linear interpolation at missing points + model predicts relative correction.  
- **Features:** donors and one-step shifts, previous and next target values.  
- **Model:** ElasticNet with iterative forward/backward filling.  

---

## Results

- ~25% improvement over linear interpolation (RMSE).  
- Stable performance even with higher missing rates.  

---
