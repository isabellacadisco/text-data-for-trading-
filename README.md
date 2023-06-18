# Text data for trading
## Machine learning in finance: forecasting and usage of large language models

This repository contains the final project of the lab conducted with [Ammagamma](https://ammagamma.com/) at [UniMi](https://www.unimi.it/it/corsi/laurea-magistrale/data-science-economics-dse). 
The project aims to leverage the use of large language models to perform a sentiment analysis of financial news to enrich a model for predicting exchange values in the forex market.


* `DistilBert_FinancialNews.ipynb` contains the fine tuning of DistilBERT on a labeled dateset of financial news on the task of sentiment analysis. `TFDistilBertForSequenceClassification` from the [HuggingFace🤗Transformers library](https://huggingface.co/docs/transformers/v4.30.0/en/model_doc/distilbert#transformers.TFDistilBertForSequenceClassification) was exploited to produce a model to classify news as positive, neutral or negative.

* `News_scraping.ipynb` contains the scraping of news from the [forexrate.co.uk](http://www.forexrate.co.uk/) website.

* `Sentiment_analysis.ipynb` exploits the classifier produced to extract the sentiment for the collected news and then aggregate it for each date.
  
* `Forecast.ipynb` contains different forecast approaches of the EURUSD exchange value expoiting the [Prophet](https://facebook.github.io/prophet/) model. The data retrieved with the sentiment analysis were used to enrich the model.

