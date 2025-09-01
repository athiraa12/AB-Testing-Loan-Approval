# AB-Testing-Loan-Approval

This project analyzes the effectiveness of two email marketing campaigns (**Campaign A – Low Interest** vs **Campaign B – Quick Approval**) using **A/B testing**.
The primary metric for conversion is **loan approval**.

##  Dataset

The dataset contains user-level campaign interaction details:

* `user_id` – Unique user identifier
* `group` – Campaign group (A or B)
* `email_subject` – Subject line used
* `opened` – Whether the email was opened (0/1)
* `clicked` – Whether the email was clicked (0/1)
* `applied` – Whether the user applied (0/1)
* `approved` – Whether the loan was approved (0/1) → **Conversion Metric**
* `credit_score`, `income_band`, `region`, `device`, `send_time` – User/engagement features

##  Methodology

1. Defined **conversion** as `approved`.
2. Calculated approval rates for both groups:

   * Campaign A: **0.44%**
   * Campaign B: **0.52%**
3. Performed a **two-proportion z-test** to compare approval rates.

##  Results

* **Z-statistic**: -0.41
* **p-value**: 0.68
* **Conclusion**: Fail to reject null hypothesis → No statistically significant difference in approval rates between Campaign A and Campaign B.

##  Tech Stack

* **Python** (pandas, numpy, scipy, matplotlib)
* Jupyter Notebook

##  Repository Structure

```
├── data/                 # Dataset (if shared)  
├── notebook.ipynb        # Analysis notebook  
├── README.md             # Documentation  
```

## Future Work

* Test alternative subject lines with larger sample size.
* Consider multi-metric evaluation (open → click → apply → approve).
* Explore segmentation (region, income band, device type).


