
# Six Sigma MarketMaster Portfolio Builder

##### Copyright 2024, Georgia Tech 
##### _All Rights Reserved_

## Course: DVA 2024 Spring Team 109



### A brief description of what this project does and who it's for: 


In our project, codes were developed for the procedures below. 

 1) **Visualization** development 

 2) Portfolio construction by **Random Forest model** 

 3) Portfolio construction by **Factor Analysis** 

 4) Prediction and Forecasting by **Support Vector Regression** 

 5) **Dynamic poster** development *Not used for presentation recording, but our **key-appendix deliverable**.

Demo of 1 through 4: https://www.youtube.com/watch?v=FLSM-afAG5o

Demo of 5:
https://www.youtube.com/watch?v=0Q5gSF3Hwd8

 Concise explanation on Description, Installation, Execution follows as below. 

 FYI: _README for each procedure is prepared in "CODE" folder as well for convenience, as appendix._ 

 

 

### 1. DESCRIPTION - Description of the package in a few paragraphs ###

 1) Visualization development: **Dash Web Trader** 


  This is a demo of the Dash interactive Python framework developed by Plotly. 

  The code and instructions to develop the App itself is stored in CODE folder. 

  Here, INSTALLATION and EXECUTION on launching the App, MarketMaster is explained. 

 

 2) Portfolio construction by **Random Forest model** 

  For Random Forest Model Building & Experiments, instructions on how to run the random forest models and get output. 

  Notes: 

   _The input data and the scripts are in the same file._ 

   _The output results and plots will be saved in the same file after running._ 

   _The 'output' file contains results already produced for reference. Depending on each running, the random forest results could differ slightly._

   _The 'merged data' file contains output results merged for analysis in the next steps._ 

 

 

 3) Portfolio construction by **Factor Analysis** 

  Includes Factor Investing and Stock Selection. 

  Selection methodology parallels the systematic approach outlined in factor investing literature. 

  By choosing high capitalization, long standing companies, aim is to capture similar benefits as those observed with size, value, profitability, and momentum. 

  The current stock portfolio offers a blend of historical performance and stability, which provides a strong foundation for a diversified portfolio. 

  Choice of stocks and sectors is supported by the lessons drawn from the extensive literature review, ensuring a balanced approach that mitigates peculiar risks while targeting market inefficiencies. 

  * _Data is obtained directly from yahoo finance - quantmod package._ 

 

 4) Prediction and Forecasting by **Support Vector Regression** 

  Required packages *R used as software 

    e1071 

    readxl 

    dplyr 

    tidyr 

    lubridate 

    zoo 

    ggplot2 

    ggpubr 

 

 5) **Dynamic poster** development 

  This is an interactive, multi-page report which displays a variety of tables, bullet points, and Plotly interactive plots in a report format. 

  The app incorporates custom local and external CSS to display distinct pages for PDF print. 

 


### 2. INSTALLATION - How to install and setup our code ### 

 1) Visualization development: **Dash Web Trader** 

  [1] Open command prompt as administrator 

  [2] run 
  
    docker pull dylanchongdy/six_sigma_market_master:latest 

[3] Open Docker Desktop 

  Install the requirements: 

    chart_studio==1.1.0 

    dash==2.15.0 

    dash_core_components==2.0.0 

    dash_html_components==2.0.0 

    Flask==2.3.2 

    numpy==1.25.1 

    pandas==2.0.3 

    plotly==5.19.0 

    Requests==2.31.0 

    scikit_learn==1.1.3 

    scikit_learn==1.4.1.post1 

 

 2) Portfolio construction by **Random Forest model** 

  Instructions on how to install and set up the project: 

   Copy the file 
   
    RF_data_code_output
   
   in the repository. 

   Install dependencies with 
   
    pip install yfinance 

   _Python version: 3.10_ 

 
 

 3) Portfolio construction by **Factor Analysis** 

  [1] Download below files. 

      Portfolio3.Rmd 

      Portfolio4.Rmd     

  [2] In the code for portfolio 3, adjust the path so that each line makes connection to the downloaded csv in step 1. 

    Line 58 - change the period to weekly and monthly as required to alter the analysis time frame if required.  

  Monthly Returns Usage: Monthly returns reduce the impact of daily market fluctuations in the analysis. 

  This approach facilitates the observation of longer-term performance trends, which are crucial for strategic investment decisions. 

  By Default it is set to weekly to observe weekly performance. 

    Line 168 - Returns for portfolio 3 - adjust the path for output, to your preferred location in your computer 

    Line 169 - Returns for S&P500 - adjust the path for output, to your preferred location in your computer 

    Line 204 - Provides return for individual tickers - adjust the path for output, to your preferred location in your computer 

  [3] In the code for portfolio 4, adjust the path so that each line makes connection to the downloaded csv in step 1. 

    Line 58 - change the period to weekly and monthly as required to alter the analysis time frame if required.  

    Line 178 - Returns for portfolio 4 - adjust the path for output, to your preferred location in your computer 

    Line 179 - Returns for S&P500 - adjust the path for output, to your preferred location in your computer 

    Line 212 - Provides return for individual tickers - adjust the path for output, to your preferred location in your computer 

 

 

 4) Prediction and Forecasting by **Support Vector Regression** 

  [1] Download below files. 

       SVR_ver_final.R 

       PF3_portfolio_returns_week.csv 

       port4_returns_week.csv 

       rf_data_for_plot_predict.csv 

       SP500_returns_weekly.csv 

  [2] In the code, line 17 - 20, adjust the path so that each line makes connection to the downloaded csv in step [1]. 

  [3] In the code, line 492 and 494, adjust the path for output, to your preferred location in your computer 

 

 

 5) **Dynamic poster** development 

  First create a virtual environment with conda or venv inside a temp folder, then activate it. 

   virtualenv venv 

    # Windows 

     venv\Scripts\activate 

    # Or Linux 

     source venv/bin/activate 

 

  install the requirements with pip 



   Install the requirements:

    chart_studio==1.1.0 

    dash==2.15.0 

    dash_core_components==2.0.0 

    dash_html_components==2.0.0 

    Flask==2.3.2 

    numpy==1.25.1 

    pandas==2.0.3 

    plotly==5.19.0 

    Requests==2.31.0 

    scikit_learn==1.1.3 

    scikit_learn==1.4.1.

    dash-cytoscape==1.0.0 

    gunicorn==19.9.0 

    requests==2.31.0 

 

 

 

 

### 3. EXECUTION - How to run a demo on our code ### 

 1) Visualization development: **Dash Web Trader**

  Back in command prompt, run below code 

    docker run -p 8051:8051 dylanchongdy/six_sigma_market_master 


  To run this app first clone repository and then open a terminal to the app folder. 

    git clone https://github.com/plotly/dash-sample-apps.git 

    cd dash-sample-apps/apps/dash-web-trader 

  Create and activate a new virtual environment (recommended) by running the following: 

 

  On Windows 

    virtualenv venv  

    \venv\scripts\activate 

  Or if using linux 

    python3 -m venv myvenv 

    source myvenv/bin/activate 

  Run the app: 
    
    python app.py 

  You can run the app on your browser at: 

    http://127.0.0.1:8051 


Notes:

_Dockerfiles may require a few attempts to adapt to various environments successfully, so please be patient and try running the build process multiple times if needed until it executes without any issues._

 2) Portfolio construction by Random Forest model 

  Steps to run 

   **Run1:**

    python3 random_forest_model1_2.py 
   
   input: 
      
      cleaned_data_503stocks.csv 
   
   output: 

      model1_2_scores.csv 
  

   **Run2:** 

    random_forest_model3_4.py

   input: 
   
    cleaned_data_503stocks.csv. 
    
  output:

    weekly_portfolio_return_model3_4.csv, model3_4_score_feature.csv 

  **Run3:** 
   
    SP500_weekly_return.py
  output: 
  
    sp500_returns_rfr_rate.csv 

  **Run4:**
   
    random_forest_experiment1.py 

  input: 
    
    weekly_portfolio_return_model3_4.csv, sp500_returns_rfr_rate.csv. 
  
  output: 
  
    experiment1_portfolio_metrics.csv 

  **Run5:** 

    random_forest_plotting.py 
  
  input: 

    weekly_portfolio_return_model3_4.csv, sp500_returns_rfr_rate.csv 
  
  output: 
  
    plot1_cumulative_return_model3.png, plot2_cumulative_return_model4.pn, plot3_weekly_median_return_model3.png, plot4_weekly_median_return_model4.png 

 

 3) Portfolio construction by **Factor Analysis** 

  Run R files

  Note: _Roughly takes 60 seconds to complete the run_.

 

 4) Prediction and Forecasting by **Support Vector Regression** 
  
  Run R files 

  Note: _Roughly takes 100 seconds to complete the run. The step for developing SVR model takes some time._ 

 

 5) Dynamic poster development 

  Run the app:

    python3 -m app_merged.py
  
  You can view the app on your browser at: 

    http://127.0.0.1:8051 