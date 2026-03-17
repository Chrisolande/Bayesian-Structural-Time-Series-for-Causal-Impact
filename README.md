# Causal Inference: COVID-19 & Food Price Volatility in Kenya [WIP]

## 📌 Project Overview
This project investigates the causal impact of COVID-19 lockdowns (March 2020) on food prices across 63 Kenyan markets. Using a single-source dataset from the **World Food Programme (WFP)**, the study identifies treatment effects through geographic variation in supply chain dependence and market remoteness.

The core of this project is **methodological triangulation**: using five distinct causal inference frameworks to ensure the estimated effects are robust to unmeasured confounding and model specification.

## 🛠 Research Strategy
The project is structured into a Quarto book covering a multi-pronged causal "attack":

1. **Identification via DAGs:** Modeling the 2019-2020 drought and fuel prices as mediators/confounders using `dagitty`.
2. **Geographic Instruments:** Computing `distance_from_nairobi` via Haversine formula to proxy for supply hub dependence.
3. **Triangulated Estimation:** Running Matching, IPW, DiD, RDD, and IV to check for sign and magnitude agreement across estimands.
4. **Bayesian Counterfactuals:** Final synthesis using `CausalImpact` (BSTS) to visualize the "What If" scenario for Nairobi.

## 📦 Tech Stack
- **Language:** R
- **Causal Frameworks:** `CausalImpact`, `bsts`, `ggdag`, `MatchIt`, `WeightIt`, `fixest`, `rdrobust`
- **Data Engineering:** `tidyverse` (dplyr, tidyr, ggplot2, sf/geosphere)
- **Reporting:** Quarto Book

## 📈 Analysis Roadmap
- [x] **Chapter 1:** Data Ingestion (WFP 2-row header parsing) & Haversine Distance Calculation.
- [x] **Chapter 2:** Causal Assumptions & DAG Construction (`dagitty`).
- [ ] **Chapter 3:** Matching (Nearest Neighbor on pre-COVID price levels/trends).
- [ ] **Chapter 4:** Inverse Probability Weighting (IPW) & Overlap Diagnostics.
- [ ] **Chapter 5:** Difference-in-Differences (Callaway-Sant'Anna for staggered timing).
- [ ] **Chapter 6:** Regression Discontinuity (200km "Curfew-Window" Cutoff).
- [ ] **Chapter 7:** Instrumental Variables (Distance as an Instrument for Exposure).
- [ ] **Chapter 8:** Sensitivity Analysis (E-values, Rosenbaum bounds, Placebo tests).
- [ ] **Chapter 9:** Bayesian Structural Time Series (BSTS) Synthesis.

---
