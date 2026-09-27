# Hierarchical Bayesian Hedonic Pricing of Used Tractors

This project develops a probabilistic pricing model for **used agricultural tractors**, using a large multi-country dataset provided by **Spectinga**.

The main goal is to estimate **realised wholesale prices** from tractor characteristics and market information, while also quantifying uncertainty around the predictions. The analysis also investigates which machine characteristics are most strongly associated with price.

## Objectives

The project focuses on two main objectives:

- Predict realised wholesale tractor prices with associated uncertainty.
- Identify the machine and market characteristics most strongly related to price variation.

A secondary analysis also investigates whether advertised **asking prices** can provide useful additional information for predicting realised prices.

## Data

The project uses proprietary data provided by **Spectinga**. The original dataset contains agricultural machinery listings and transaction records from multiple countries, together with technical specifications and market information.

See the [`Data/README.md`](./Data/README.md) file for further details.

## Methodology

The analysis is based on a **Bayesian hedonic pricing framework** estimated using **Integrated Nested Laplace Approximation (INLA)**.

Several model specifications are compared, progressively introducing:

- fixed effects for tractor characteristics;
- hierarchical effects for **manufacturer, model series and country**;
- a monthly temporal component;
- a joint model combining realised and asking prices;
- a robust **Student-t likelihood** to reduce the influence of extreme observations.

Predictors include variables such as **age, operating hours, horsepower, transmission, GPS equipment and optional features**.

Model performance is assessed using both predictive and Bayesian criteria, including **R², RMSE, MAE, MAPE, DIC, WAIC and NLSCPO**.

## Main findings

The hierarchical structure provides the largest improvement in predictive performance, showing that **manufacturer, model series and country capture substantial price heterogeneity** beyond the observed tractor characteristics.

The results also show that:

- older tractors and tractors with more operating hours tend to have lower prices;
- horsepower is positively associated with price;
- selected equipment, particularly **front loaders**, is associated with higher values;
- asking prices are substantially higher on average than comparable realised wholesale prices;
- the Student-t specification provides a more robust fit in the presence of extreme observations.

The final model explains approximately **93% of the in-sample variation in log prices**, while retaining meaningful predictive performance on a chronological test set.

For a complete overview of the project, see [`Report/s2882823_last_version.pdf`](./Report/s2882823_last_version.pdf).
