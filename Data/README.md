## Data

This project uses a proprietary dataset provided by **Spectinga**, an agricultural machinery marketplace and data provider. The data contain listings and transaction records for agricultural machinery across multiple countries, together with detailed machine characteristics and market information.

### Spectinga market listings dataset

The original `market_listings.csv` dataset contains **354,607 observations**, approximately **79% of which are tractors**. Since this project focuses on tractor pricing, only tractor observations were retained. The raw dataset contains 46 variables describing machine characteristics, sales channel and observation date.

Two main analytical datasets were constructed:

- **Realised-price dataset** — contains wholesale transaction prices from completed sales and is used as the main dataset for model estimation and evaluation.
- **Asking-price dataset** — contains advertised listing prices and is used to investigate the relationship between asking and realised prices.

The variables used in the analysis include tractor **age, operating hours, horsepower, transmission, GPS equipment and other technical features**, together with **manufacturer, model series, country and transaction date**.

### Data availability

The **raw datasets are not included in this repository**. The data were provided by Spectinga for the purposes of this project and cannot be redistributed publicly.

