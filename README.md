# Data-Driven Product Optimization Using A/B Testing & User Engagement Analytics
---
### __🎯Project Overview__
---
Modern digital platforms rely heavily on controlled experimentation to guide product decisions and improve user experience. This project simulates a real-world product experimentation scenario by analyzing user engagement data from two website variants — a Control version and an Experimental version.
The dataset captures session-level behavioral signals such as click activity, session duration, device usage, referral channels, and interaction timestamps. The project focuses on cleaning noisy real-world data, validating experiment integrity, and applying statistical testing methods to evaluate whether the experimental design significantly improves user engagement.
Beyond statistical testing, the project emphasizes product thinking by interpreting results in terms of user behavior, feature performance, and business impact. The analysis demonstrates how experimentation frameworks can guide feature rollouts, optimize user journeys, and improve conversion outcomes.

### __🔍Key Findings__
---
- The experimental variant increased click-through rate from ~20% to ~50%, delivering an absolute lift of ~29.5 percentage points (~1.46× relative improvement).
- Statistical testing confirmed the improvement is highly significant (Z ≈ 137, p < 0.001), indicating the effect is not due to random variation.
- The uplift remained consistent across devices, referral sources, and time-of-day segments, suggesting a broadly effective design change.
- Engagement quality remained stable: while mean session time slightly decreased, median session time was unchanged, indicating no negative impact on typical user experience.
- Sensitivity analyses confirmed results remain stable under subsampling and metric variations, strengthening confidence in the findings.
- The results suggest the experimental design meaningfully improves user engagement and is suitable for rollout.

### __🗂️Dataset__
---
We have used [Simulated A/B Testing Dataset](https://www.kaggle.com/datasets/sanxhi/ab-testing-data-simulated-web-user-engagement) from kaggle to understand user behavior, experimentation, and product decision-making. The dataser contains about 200k records where each row represents an individual user session, with attributes capturing click behavior, session duration, access device, referral source, and timestamp.

| Features               | Features defination                                                        |
|------------------------|----------------------------------------------------------------------------|
|click                   |Binary (1 if clicked, 0 if not)                                             |
|group                   |A/B group assignment (con or exp, with injected label inconsistencies)      |
|session_time            |Time spent in the session (in minutes), including outliers                  |
|click_time              |Timestamp of user interaction (nullable)                                    |
|device_type             |Device used (mobile or desktop, mixed casing)                               |
|referral_source         |Where the user came from (e.g., social, email, with some typos/whitespace)  |

### __⚙️Methods__
---
-__Data Loading & Setup__
-__Data Cleaning & Preprocessing__
-__Experiment Context & Goal__
--Sample Ratio Mismatch (SRM) check
--Define hypotheses
--Compute the key metrics
--Confidence Interval (CI)
--Z-test
-__Robustness, Segmentation & Sensitivity Analysis__
--Guardrail Metrics (Engagement)
--Heterogeneous Treatment Effects (HTE)
--Temporal Robustness (Time-based Checks)
--Sensitivity Analysis
--__Decision Making__

### __🛠️Tools & Technologies__
---
-__Programming Language:__ Python
-__Libraries:__ NumPy, Pandas, Seaborn, Matplotlib, Statsmodels
-__Environment:__ Google Colab
