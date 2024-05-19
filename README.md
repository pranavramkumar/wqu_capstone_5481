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
  * **Motivation**: asda
  * **Goals**: asdas
  * **Unique contributions to literature**: asdas
  * **Lessons learnt**: asdas

## Project Scope
*In scope:*
1. What does it mean to be a full-stack web developer?
2. What is the relationship between HTML and CSS?
3. What is

*Out of scope:*
1. What does it mean to be a full-stack web developer?
2. What is the relationship between HTML and CSS?
3. What i


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
   5.3 Vintage </br>
   5.4 Localized Effects </br>
   5.5 Climate Scenarios </br>
   5.6 Market Structure Changes and Long Term Forecasts </br>
   5.7 Constrained Optimization </br>
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

## Links to useful prior carbon price forecasting literature
* [Version Control](https://en.wikipedia.org/wiki/Version_control)
* [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
* [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
* [Pro Git](https://git-scm.com/book/en/v2)
* [Dev Docs](https://devdocs.io/)
  
## How to contribute to this project
As you can see from the accompanying paper, there are severe limitations to the way the data has been sourced, the feature set considered, the model train-test splits and validation routines (doesn't include walk-forward, cpcv or kcv validations), and 


- - -
© 2024 Pranav Ramkumar, Artis Jhamar Johnson and Ekoue Jean Kougnah. brand. All Rights Reserved.
