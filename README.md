# Predicting Audience Attitudes and Behavior from the News

## Background 

When it comes to data, the social impact world does not have the kind of access the private sector has to drive decision making and innovation. Unstructured data from news, social media, and websites, however, provides a rich, open source for developing insights that can drive transformative social change. I am all too familiar with this challenge, having committed the last decade of my professional life to applying data and technology to affect positive social change. 

Understanding public narratives around civic engagement, which the media plays an important role in shaping, has been a central theme of this work. As a result, I decided to focus this project on how we can apply natural language processing and predictive modeling to look at how media influences the beliefs, attitudes ,and behaviors of audiences. 

Based on this logic, I sought to answer the question:

  * *Can we use political news to predict how people might feel in the future about political or civic issues?* 

This respository contains the documentation and code to answer this question. 

## Modeling the News

The goal of this project is to attempt to predict future google search volume for the word depression, based on American political news in the present.

For my final model, my goal was to use hourly aggregated political news tokens derived from 12 prominent media outlets to predict binarized (high or low) Google search volume for "depression" 12 hours later.  

My final model, built with tensorflow, used a Google News pretrained word embedding layer, followed by three hidden dense layers with descending nodes (16, 8, 4) and dropout on the final layer. 

My final train accuracy was 82 percent and my final test accuracy was 81 percent, which means my model correctly predicted high or low search volume 81 percent of the time. Given that this was a rather challenging prediction task, I consider this an extremely promising result.

The implication here is that there does seem to be a relationship between political news and how audiences feel after reading the news. It also seems to suggest that we can predict, to some degree, how political news from today affects people tomorrow, even if it is a rather simple way of describing those behaviors.

## Application in the Wild

While this is very much a prototype, it provides a potentially new template to assess the impact of media and narratives on audiences, which is important in the civic change space. Covid is a great example of how this might be helpful. With some creative tinkering, we could use an approach like this to analyze how covid is presented in the media, predict how it might impact people, and then use those insights to head off destructive narratives.

## Documentation, Code, and Data

Detailed project description, methodology, data dictionary, and findings [here]()

Video description of final model and results [here](https://www.youtube.com/watch?v=LGNBgSgDZ0E&feature=youtu.be) (Youtube video)

Final trained model [here](https://drive.google.com/drive/folders/1Q-KY_vrxwUrRKOyU2SpXJh_uHUsE9-at?usp=sharing)    (tensorflow saved_model.pb with weights)

Final aggregated and preprocessed dataset used to train the model [here](https://drive.google.com/file/d/1w8SQ0RGEl90wnfCKHj5gcB57K8n0dozb/view?usp=sharing) (CSV).

Jupyter notebook used to train the final model [here](https://github.com/AschHarwood/predicting_attitudes_from_news/blob/master/notebooks/NN_Training_Trends_25k_12hrs_Final_12_17_20.ipynb) (IPYNB)

Conda virtual environment to configure your own environment if you want to test the model yourself [here](https://github.com/AschHarwood/predicting_attitudes_from_news/blob/master/docs/environment.yaml)

Collection of jupyter notebooks for scraping, preprocessing, eda, and modeling [here](https://github.com/AschHarwood/predicting_attitudes_from_news/tree/master/notebooks/final_report_notebooks) and description of this collection [here](https://github.com/AschHarwood/predicting_attitudes_from_news/blob/master/docs/Asch_Harwood_Read_Me_Capstone_Code_Reference%20copy.txt)

Roughly 200,000 lightly processed, unaggregated political news articles with GDELT tone scores, March 2015 - October 2020 [here](https://drive.google.com/file/d/1Z7VFhfCPKLXBt-rMbGH3Ici4agQy_Wud/view?usp=sharing)
