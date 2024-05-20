# Forcasting carbon allowance prices across five emissions trading systems using deep learning (2017-2023)


## Essential information
![WQU Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/7/72/WQU_logo_color.png/440px-WQU_logo_color.png)
> This is the open Git repo for the WorldQuant University Capstone Final Project Submission for Group 5481 </br>
The group members included Pranav Ramkumar, Artis Jhamar Johnson and Ekoue Jean Kougnah </br>
Pranav focussed on datasets, Artis focussed on model-selection and model training, and Kougnah focussed on literature review

## Technologies used
`GoogleSheets` was used as the datasheet to assemble the feature vectors and target matrix into datasets </br>
`Python-based` preprocessing tools, and data aggregators were used for curating individual vector data </br>
`Python` and its libraries have been used as the tool of choice for exploratory analysis and deep learning based modeling and forecasting of carbon allowance prices. </br>
The following libraries are required to execute the .ipynb files in this git repo: 
  * os, csv, sys, and drive from google.colab (optionally to mount google drive path)
  * numpy, pandas,datetime, math
  * matplotlib (specifically pyplot, mdates, mpatches, LineCollection, Colormap, ListedColormap, BoundaryNorm, MonthLocator, DateFormatter)
  * seaborn
  * yfinance, pandas_datareader
  * statsmodels - seasonal_decompose (from seasonal), SimpleExpSmoothing and ExponentialSmoothing (from holtwinters)
  * tensorflow, xgboost (XGBRegressor)
  * torch, torch.optim, torch.nn
  * CEEMDAN_LSTM
  * sklean.model_selection (train_test_split, GridSearchCV, cross_val_score, RepeatedKFold)
  * sklearn.metrics (mean_absolute_error, mean_squared_error, mean_absolute_percentage_error)
  * tensorflow.keras.layers (Dense, Activation, Dropout, LSTM, GRU, Flatten, BatchNormalization)
  * tensorflow.keras.models (Sequential, load_model)
  * tensorflow.keras.optimizers (Adam)
  * tensforflow.keras.callbacks (ReduceLROnPlateau, EarlyStopping, ModelCheckpoint)

## Git repo structure
The data folder contains:
* `raw` folder > contains the datasets for RGGI, California, Korea, EU-ETS and China with headers extended feature sets; also contains an .xlsx consolidate file with links in headers to official data sources used
* `processed` folder > only the target vector and feature matrix (X1-X14) selected for model-fit and forecasting
* `pre-processing` folder > contains pre-processing done before assembling vectors into dataset in .xlsx format (which includes linear-model estimations)
  
The git repo contains:
* Accompanying paper in .pdf format
* `ExploratoryAnalysis.ipynb` which encompasses all exploratory inquiries asked of carbon allowances prices as an asset class
* `Diagnostics.ipynb` which contains stationarity, collinearity and trend analysis of individual vectors within each dataset
* `Forecasting.ipynb` which contains model definitions, model-fit, hyperparameter optimization and loss-function reporting for all models

## Project Information
Here is some outlining information about the project:
  * **Motivation**: The motivation for this research is to bring financial engineering skillsets to the field of carbon pricing </br></br>
  * **Goals**: The goal is to demonstrate how carbon allowance prices may be forecasted using some popular machine learning models with the view to construct portfolios of allowances using spot or futures instruments to securitize an ETF for institutional investors </br></br>
  * **Unique contributions to literature**:
    * Prior literature hasn't covered multiple ETSs across countries to take comparative views
    * Prior literature hasn't applied transformer models to the domain of carbon price forecasting
    * There have been very few papers which have disussed or demonstrated an investment portfolio approach using carbon price forecasts </br></br>
  * **Lessons learnt**:
     * Complexity is high and it's better to split up portfolio construction and back-testing into a different paper
     * Extra attention to feature selection, cross-validation routines and model tuning can likely improve model performance
     * The lack of a structured data pipeline in the compliance markets is a significant to barrier to commercialization 

## Project Scope
*In scope:*
1. Five ETSs namely - RGGI, California Cap and Trade, Korea, EU ETS, and China ETS (average of Beijing and Shanghai pilots)
2. Exploratory analysis to establish that a 'Carbon Allowance ETF' presents a diversified asset class for institutional investors
3. Study of historical regulatory policies of the five ETSs, to investigate if investing in five ETSs smoothens the stresses from one
4. Predicting allowance prices into the future for five ETSs with 3 different model types (CEEMDAN-LSTM, XGBoost and Transformer)
5. Reporting three different loss functions in and out of sample namely MAE, RMSE and MAPE

*Out of scope:*
1. Extensive Feature Engineering: does not include energy-system variables, or NLP-based feature engineering
2. ETF Construction: Methods to construct an ETF as a portfolio of spot allowances, or allowance futures using portfolio optimization methods and benchmark portfolios
3. Scenario Development for Long-Term Forecasts: Feature Vectors have not been forecasted into the future using expert judgment and priors, statistical methods (like cholesky decomposition), or from predictions generated by macroforecasting or climate forecasting models
4. Carrying out long-term forecasts (out to 2030 or 2050) and back-testing financial and environmental impact of the carbon ETF constructed


## Table of Contents of accompanying paper
1. Introduction </br>
   1.1 Background - The field of carbon pricing, Emissions control mechanisms </br>
   1.2 Literature Review - Emissions trading systems, Carbon price forecasting </br>
2. Data </br>
   2.1 Data Availability </br>
   2.2 Feature Selection </br>
   2.3 Data Preprocessing </br>
3. Methodology </br>
   3.1 CEEMDAN-LSTM </br>
   3.2 Boosting and XGBoost </br>
   3.3 Transformers </br>
   3.4 Train-Test splits used </br>
   3.5 Loss functions used </br>
4. Results </br>
   4.1 Exploratory Analysis </br>
   4.2 Diagnostics </br>
   4.3 Forecasting </br>
5. Discussions </br>
   5.1 Environmental ETF Design </br>
   5.2 Environmental ETF Construction </br>
   5.3 Climate Scenarios </br>
   5.4 Long Term Forecasts </br>
6. Conclusions </br>
A. Appendix A: Literature Review - Emissions Trading Systems </br>
B. Appendix B: Literature Review - Carbon Price Forecasting </br>
C. Appendix C: Data Dictionary </br>
D1. Appendix D1: Code for CEEMDAN-LSTM Model </br>
D2. Appendix D2: Code for XGBoost Model </br>
D3. Appendix D3: Code for Transformer Model </br>
E. Appendix E: Results Detailed </br>
F. Appendix F: Literature Review - Environmental ETF Design </br>
G. Appendix G: Climate Scenarios </br>
Acknowledgements </br>
7. References </br>

## Links to some useful prior carbon price forecasting literature
* [Lu, Ma and Azimi (2020) "Carbon trading volume and price forecasting in China using multiple machine learning models"](https://www.researchgate.net/publication/337331915_Carbon_trading_volume_and_price_forecasting_in_China_using_multiple_machine_learning_models)
* [Yang et al (2021) "An Ensemble Prediction System Based on Artificial Neural Networks and Deep Learning Methods for Deterministic and Probabilistic Carbon Price Forecasting"](https://www.researcher-app.com/paper/8762007)
* [Yun et al (2022) "Forecasting carbon dioxide emission price using a novel mode decomposition machine learning hybrid model of CEEMDAN-LSTM"](https://onlinelibrary.wiley.com/doi/10.1002/ese3.1304)
* [Tan et al (2022) "Forecasting European carbon returns using dimension reduction techniques: Commodity versus financial fundamentals"](https://www.sciencedirect.com/science/article/abs/pii/S0169207021001163?via%3Dihub)
* [Shahzad et al (2023) "Forecasting carbon emissions future prices using the machine learning methods"](https://link.springer.com/article/10.1007/s10479-023-05188-7)
* [Zhang et al (2023) "Carbon trading and COVID-19: a hybrid machine learning approach for international carbon price forecasting"](https://link.springer.com/article/10.1007/s10479-023-05327-0)
* [Feng et al (2023) "Carbon price prediction based on decomposition technique and extreme gradient boosting optimized by the grey wolf optimizer algorithm"](https://www.nature.com/articles/s41598-023-45524-2)
  
## How to contribute to this project
As you can see from the accompanying paper, there are severe limitations to the way the data has been sourced, the feature set considered, the model train-test splits and validation routines (doesn't include walk-forward, cpcv or kcv validations), and how an ETF has been constructed using the forecasts. Given the future scope of this project, if you would like to take this work further and collaborate with the authors, contact Pranav by raising a new issue. 


- - -
© 2024 Pranav Ramkumar, Artis Jhamar Johnson and Ekoue Jean Kougnah. brand. All Rights Reserved.
