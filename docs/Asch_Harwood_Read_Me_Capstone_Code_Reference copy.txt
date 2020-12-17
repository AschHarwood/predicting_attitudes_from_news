Asch Harwood
BrainStation DS Program
Capstone Final Report
November 1, 2020


Code Reference document
Data Acquisition and Cleaning


Example of one of the many scrappers used to extract article text based on URLs from GDELT dataset, which provided dates, themes, tonal scores, and urls but does not provide text.


* article_scrapper_example_final_report_oct_28.ipynb


Basic cleaning script for GDELT data extracted via the GDELT python package to be passed to article scraper


* gdelt_missing_data_cleaing_Oct_18.ipynb




Scraping URLs from GDELT via its python package


* Gdelt_scraping_python.ipynb


Querying Google Trends API


* Google_trends_scraping-final_report.ipynb


Light EDA and cleaning of Google Trends data


* Gtrend_exploration.ipynb


Joining and cleaning and final transformations for V5 complete dataset
* gdelt_scrape_article_join_Oct_22.ipynb


Reviewing tokens in article corpus


* Bag_of_Words_Analysis.ipynb


Clean up of Gallup monthly data. This dataset is part of V4 iteration as a potential target.


* Cleaning_Gallup_Monthly_GDELT_Joining_timeseries.ipynb


Visual of exploration of final dataset in Tableau. Used to prepare charts for presentation




Models
V1_Data: 5,000 articles on climate change, Target: GDELT polarity, Row: individual article
Original MVP toy model using just 5000 articles about climate change. Includes two approaches: using the entire article text to predict polarity, and using speaker quotes only to predict polarity.


* Gdelt_Polarity_Target_LogReg_5000k_Reviewed_OCt_25.ipynb
V2_Data: Target: GDELT Sentiment, Row: individual article


MVP model using bag of words and logistic regression. Features were individual article tokens and target was sentiment score provided by GDELT. I achieved decent results with minimal work, which gave me confidence to move on to trying to predict external sentiment and Google Trends.


* CountVect_TFIDF__NGRAMS_Log_Reg_Full_Text_Tone_Target_Oct_12_reviewed_Oct_25.ipynb


First neural net prototype
* Neural_net_v1.ipynb


V3_Data: Target: Brandwatch Sentiment, Row = Daily articles, Time: 2018 - 2020


Gridsearch with H2O automl, earlier version of dataset, daily aggregation, 2018 - 2020, target = Brandwatch sentiment, no shift


* Auto_ML_H2O_Day_GDELT_BW-Sent__Oct_13_Reviewed_Oct_25.ipynb


Gridsearch with earlier version of dataset, daily aggregation, 2018 - 2020, target = Brandwatch sentiment, no shift


* Grid_Search_Sentiment_Weekly_Oct_12_review_Oct_25.ipynb


Neural Net Regression and Neural Net with TF-IDF
* joing_bw_with_text_neural_net_oct_11.ipynb


V4_Data: Target: Google Trend, Row: Hourly articles, Time: 2015 - 2020 w/ gaps


Logistic Regression with TF-IDF on hourly data, no in shift with target, i.e. 10 am news would be predicting 10 am google search. Also, this particular version of the dataset had a 9 month gap in text, which I had to go back and fill.


* LogReg_TFIDF_Gdelt_Text_Gtrends_Hourly_Oct_18_reviewed_Oct_25.ipynb


Variations of bag-of-words, ngrams, and Naive Bayes and Logistic Regression on hourly data, no in shift with target, i.e. 10 am news would be predicting 10 am google search. Also, this particular version of the dataset had a 9 month gap in text, which I had to go back and fill


* NB_Gdelt_Text_Gtrends_Hourly_Oct_18-Copy1.ipynb




Neural Net, hourly data, 24 hr shift


* Neural_Net_Text_GTrends_Embeddings_OCt_20.ipynb
V5_Data: Target: Google Trend, Row: Hourly articles, Time: 2015 - 2020, 12 hour shift


Rerun of logistic regression with grid search on final iteration of complete dataset, 2015-2020, hourly aggregation,  target = Google Trends, shifted 12 hours


* Logistic_regression_final_dataset_final_report.ipynb


Final Neural Net 


* NN_Training_Trends_25k_12hrs_Oct_23-Copy1.ipynb


Ludwig with Bert and GloVe


* Ludwig-text_metadata_Oct_23.ipynb


Folder with results and configurations for Parrell CNN, RNN, LSTM, GloVe, and Bert. I spent a lot of time tinkering and overwrote code because Ludwig automatically generates results folder.


* Ludwig_Model_Results