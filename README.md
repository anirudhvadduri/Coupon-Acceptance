# Coupon Acceptance Analysis

This portfolio project examines which driving-scenario characteristics are associated with accepting a mobile restaurant or beverage coupon. The analysis uses the **In-Vehicle Coupon Recommendation** dataset from the UCI Machine Learning Repository. It contains 12,684 survey responses in which a participant was presented with a coupon while driving in a described scenario and indicated whether they would accept it.

## What this project answers

The notebook compares customers who accepted coupons with customers who rejected them. It includes an overall review of coupon acceptance, a focused analysis of bar coupons, and an independent investigation of coffee-house coupons. The analysis uses `pandas` for summaries and `Matplotlib` and `Seaborn` for visualizations.

## Key findings

| Area                     |                                                                                                                                                                            Result | What it suggests                                                                               |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | ---------------------------------------------------------------------------------------------- |
| Overall acceptance       |                                                                                                                            7,210 of 12,684 offers were accepted (**56.8%**) | Coupon acceptance is common but far from uniform.                                              |
| Coupon type              |            Carry-out/take-away offers had **73.5%** acceptance and inexpensive restaurant offers had **70.7%** acceptance; bar offers had **41.0%** acceptance. | Offer category is an important initial targeting decision.                                     |
| Bar visiting frequency   | Drivers visiting bars more than three times per month accepted **76.9%** of bar coupons, compared with **37.1%** for drivers visiting three or fewer times per month. | Previous bar-going behavior is a useful descriptive signal for bar-offer targeting.            |
| Bar-profile comparison   |                           Drivers who went to bars more than once a month and were over 25 accepted **69.5%** of bar coupons, compared with **33.5%** for all others. | Combining behavioral and contextual indicators can identify higher-response audience segments. |
| Coffee-house habits      |                                    Frequent coffee visitors accepted **67.5%** of coffee-house coupons, compared with **45.0%** for other reported visit frequencies. | Prior venue engagement is associated with coffee-coupon acceptance.                            |
| Coffee-offer flexibility |                                                                A one-day coffee-house expiration had **58.4%** acceptance versus **43.2%** for a two-hour expiration. | More time to redeem an offer may reduce friction.                                              |

## Recommendations

The data support prioritizing carry-out/take-away and inexpensive-restaurant coupons when a campaign needs broad acceptance. Bar coupons should be targeted more selectively toward customers with a demonstrated bar-going habit and compatible travel context, such as no child passenger. For coffee-house campaigns, consider longer expiration periods and prioritize nearby venues, while using prior coffee-house frequency as a behavioral signal.

These recommendations should be validated through a randomized experiment before operational use. The underlying data are stated-intention survey responses, not recorded purchase transactions.

## Repository contents

| File                                                | Description                                                                                                                               |
| --------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `Practical_Application_1_Coupon_Acceptance.ipynb` | Completed, executed analysis notebook containing all assignment questions, data summaries, visualizations, findings, and recommendations. |
| `coupons.csv`                                     | Input dataset supplied for the assignment.                                                                                                |
| `README.md`                                       | This nontechnical project summary.                                                                                                        |

## How to run the analysis

Create an environment with Python 3 and install the required packages:

```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels jupyter
```

Then open `Practical_Application_1_Coupon_Acceptance.ipynb` in Jupyter Notebook or JupyterLab and run all cells. The notebook looks for `coupons.csv` in the repository root.

## Data source

The UCI repository describes the dataset as an Amazon Mechanical Turk survey that presents driving scenarios with contextual features such as destination, time, weather, and passengers, then asks whether the driver would accept a coupon.[1][1]

[1]: https://archive.ics.uci.edu/dataset/603/in+vehicle+coupon+recommendation
