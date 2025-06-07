# 🚗 Vehicle Insurance Claims Prediction – Project Report

## 🎯 Objective
To classify whether a customer is likely to make an insurance claim based on demographic and driving data.

---

## 📊 Dataset Summary
- **Rows:** 10,000
- **Features:** 18 (after dropping ID and postal code)
- **Target:** `OUTCOME` (0 = No Claim, 1 = Claim)
- **Each Row Represents:** An insurance policyholder

---

## 🧹 Data Cleaning
- Handled missing values in:
  - `CREDIT_SCORE` (filled with mean)
  - `ANNUAL_MILEAGE` (filled with mean)
- Label encoded categorical features

---

## 🔍 Exploratory Insights

### Claims Distribution
Most policyholders did **not** file a claim, indicating class imbalance.

### Claim Rate by Age and Experience
- Younger and less experienced drivers have a **higher claim rate**
- Claim rate decreases with **increased driving experience**

---

## 🧠 Model Training
- Model: **Random Forest Classifier** (default config)
- Split: 75% Train / 25% Test
- Evaluation: Balanced, performs well on detecting claim patterns

---

## ⭐ Top 10 Features by Permutation Importance

| Rank | Feature               | Importance |
|------|------------------------|------------|
| 1    | DRIVING_EXPERIENCE     | 0.06620    |
| 2    | VEHICLE_OWNERSHIP      | 0.04416    |
| 3    | VEHICLE_YEAR           | 0.04288    |
| 4    | GENDER                 | 0.01156    |
| 5    | PAST_ACCIDENTS         | 0.00652    |
| 6    | MARRIED                | 0.00504    |
| 7    | RACE                   | 0.00348    |
| 8    | SPEEDING_VIOLATIONS    | 0.00188    |
| 9    | AGE                    | 0.00140    |
| 10   | ANNUAL_MILEAGE         | 0.00076    |

---

## 📈 Key Business Insights

### 🔸 Driving Experience vs Claims
> Drivers with **less experience** are significantly more likely to file claims.  
🟢 *Suggestion:* Target experienced drivers with lower premiums.

### 🔸 Vehicle Ownership vs Claims
> Customers who **don’t own** the vehicle have a higher claim rate.  
🟢 *Suggestion:* Include vehicle ownership as a risk factor in pricing.

---

## ✅ Conclusion
The analysis highlights clear patterns between driver experience, ownership status, and claim likelihood. These insights support smarter policy pricing and risk mitigation strategies.

