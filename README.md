# TASK 01: Food Delivery Delay Pattern Investigation

## 1. Problem Statement
Food delivery platforms experience thousands of orders daily. Recently, customer complaints regarding late deliveries increased by 22%. This investigation aims to identify hidden delivery delay patterns using statistical methods and exploratory data analysis to provide actionable insights for the operations team.

## 2. Dataset Description
A synthetic dataset containing 1,000 unique food delivery transactions was generated with the following attributes:
- `Order_ID`: Unique identifier for each order.
- `Distance_km`: Trip distance from restaurant to customer.
- `Prep_Time_min`: Food preparation time at the restaurant.
- `Traffic_Level`: Categorical traffic density (Low, Medium, High).
- `Weather`: Weather environment (Clear, Rainy, Windy).
- `Rating_Partner`: Delivery partner performance score.
- `City`: City location (Chennai, Bangalore, Mumbai).
- `Delivery_Delay_min`: Total delivery delay in minutes (Target Variable).

## 3. Methodology
- **Exploratory Data Analysis (EDA):** Checking missing values, duplicates, and feature data types.
- **Descriptive Statistics:** Calculating central tendency measures (Mean, Median, Std Dev, Variance).
- **Outlier Detection:** Identifying extreme delay cases using IQR/Box Plot techniques.
- **Hypothesis Testing:** Conducting One-way ANOVA to study categorical impacts on delay parameters.

## 4. Statistical Analysis & Findings
- **Average Delay:** The average delivery delay is **1.72 minutes**.
- **Distribution:** The delay distribution is highly **right-skewed (Skewness: 2.59)**, meaning while most deliveries are on time, certain factors trigger heavy unexpected delays.
- **Outliers:** The Box Plot successfully highlights atypical delay points extending beyond standard operational limits, primarily driven by external constraints.

## 5. Visualizations
The output images are saved under the `images/` directory:
1. `delay_boxplot.png` - Evaluates distribution properties and outlier limits.
2. `traffic_vs_delay.png` - Highlights delay fluctuations against traffic volumes.
3. `city_vs_delay.png` - Illustrates the average breakdown of delays per city structure.

## 6. Hypothesis Testing Results
- **Null Hypothesis (H0):** Weather does not affect delivery delay.
- **Alternative Hypothesis (H1):** Weather significantly affects delivery delay.
- **Test Conducted:** One-way ANOVA.
- **Business Interpretation:** The calculated P-Value (p < 0.05) forces the rejection of the Null Hypothesis (H0). Bad weather conditions (like heavy rain) statistically expand delivery times dramatically.

## 7. Business Recommendations
1. **Dynamic Scheduling during Bad Weather:** Proactively expand estimated delivery times (ETAs) by 12–15 minutes automatically during rains to control expectations and lower refund claims.
2. **Traffic Surge Matrix:** Deploy a higher volume of localized riders in 'High Traffic' zones during peak hours to shorten distance lapses.
3. **Optimized Buffers:** Partner ratings indicate top-tier delivery personnel process routes quicker; prioritize routing critical or high-distance orders to experienced partners.

## 8. Future Improvements
- Implement real-time machine learning models (XGBoost/Random Forest) to predict delivery time matrices dynamically.
- Integrate GPS-enabled live traffic APIs for high-resolution route optimization.
-