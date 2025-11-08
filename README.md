# Causal Impact Simulation

This project evaluates how well different causal inference methods can recover a known treatment effect using simulated, observational-style panel data.

## Methods_application 

We simulate the introduction of a scooter-sharing service in Region 8 starting in 2018, which results in a 25% synthetic drop in taxi ownership. This artificial effect is injected into otherwise realistic regional panel data, mimicking official statistics from Sweden (SCB) for the period 2002–2024.

Data Source: Statistics Sweden (SCB) from 2002 to 2024 

Artificial treatment: Taxi numbers are synthetically reduced by 25% post-treatment to simulate a real effect for 8 Region from 2018

Several causal inference methods are compared:

- Difference-in-Differences (DiD)
- Synthetic Control Method (SCM)
- Bayesian Structural Time Series (BSTS)

Control Regions were chosen with Nearest Neighbor Matching (NNM) and Propensity Score Matching (PSM) methods 

Goals:

- Simulate a realistic policy intervention.
- Evaluate performance, robustness, and interpretability of each method.
- Understand statistical significance through permutation tests and metrics

## Propensity_score 

We simulated the data and wanted to answer a question: to evaluate the effect of a **loyalty program** on customer spending. But the bias is that customers who join the program are **not random** — they are typically more active and higher-spending even before enrollment. 

Several methods have been considered:
- Propensity score 
- Inverse Probability of Treatment Weighting (IPTW)
- DoWhy Framework 

## Uplift Modeling 

The basic idea is that we know ATE thanks to our A/B tests, but we also want to know CATE in order to maximize profits and attract only the right customers, rather than bothering people who don't want it.