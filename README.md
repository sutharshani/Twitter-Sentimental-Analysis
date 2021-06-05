# Twitter-Sentimental-Analysis
In this research, we performed sentiment analysis of COVID-19 vaccine tweets using supervised machine learning approach. Social media is extensively used as a common platform to spread news and opinions. Identification of opinions towards COVID-19 vaccines would allow evidence-based decision making for better counsel and distribution of vaccines. Using social networking site Twitter, tweets from across the world were extracted for a set of vaccine related keywords. These tweets were gathered from Nov-2020 to March-2021. A random sample of the whole dataset was cleaned by applying text pre-processing techniques. As tweets contain emoticons and short words, it is difficult to correctly recognize the context of the tweets. To overcome this issue dataset with existing sentiment labels was used to train the models. Tweet sentiments are classified into three categories Positive, Negative, and Neutral. The sentiments were annotated and supervised learning methods RNNs (Single LSTM and Bidirectional LSTM) and 1D CNN were applied to train the tweet training dataset. Performance of the classifiers is evaluated on accuracy. With Bidirectional LSTM model, we achieved 74% accuracy, and it was used to implement on the COVID-19 vaccine tweets dataset.

# Table of Contents
1. [Introduction](#introduction)
2. [Data Background](#data-background)
3. [Prerequisite](#prerequisite)
4. [Project Status](#project-status)
5. [Versioning](#versioning)
6. [Authors](#authors)
7. [Acknowledgement](#acknowledgement)
8. [Reference](#reference)

## Introduction
The year 2020 was full of COVID-19 spread across the world, multiple lockdowns, and burnout of essential workers. So far, 2021 has been focused on vaccine distribution. March 11, 2021 was the first anniversary since WHO declared COVID-19 as a global pandemic [5]. As everyone wanted to go back to normal life, people were closely monitoring vaccine developments. During the lockdown COVID-19 news spread was enormously amplified in social networking platforms. Being a highly popular social platform, Twitter provides a large scale of text data for various research such as sentiment analysis [14]. Involvement of individual views and biasness in the vast fragment of these news, is giving growth to (un)intended fake information, negativity, and ambiguity in the human society [15]. These circumstances are gathering attention of researchers to carry out computational study for forming a complete representation. This research is focused on sentiment analysis of COVID-19 vaccine tweets using supervised machine learning approach. Due to the overflowing COVID-19 news and speedy development of a vaccine, people rationally have many questions on vaccines. Some of them are [6]:
-       Do the mRNA vaccines change your DNA? 
-       Did the vaccine clinical trials skip steps to be completed faster? 
-       Can the vaccine give you COVID-19? 
-       Will we need new vaccines if the virus continues to mutate?
Such questions and limited reliable answers lead to confusion and doubts overtaking the vaccine. As per Panacea lab, [7] every day, there are about 4 million tweets a day related to COVID-19. This study utilizes tweets to understand people’s sentiments. It will help understand the difference in sentiments for different vaccines and the change in sentiments over time. 
These days Natural Language Processing (NLP) is the breeding ground of research in Data Science. Sentiment analysis is one of the most common divisions of NLP. This domain has diversified the way businesses work due to extensive application usage in creating market strategies, opinion polls, chatbots, etc. For sentiment analysis, NLP has made the processing of thousands of text documents in seconds, which will take hours to process manually. The major work in this project is to clean the text data and train the model to understand the language of Twitter. As tweets contain emoticons and short words, it is difficult to correctly recognize the context of the tweets. Tweet sentiments are classified into three types Positive, Negative, and Neutral. The COVID-19 vaccine tweets dataset contains tweets from all over the world. To train and help the model to understand the tweet language, tweets dataset with existing sentiment classifications was used. After training the model, the best model was applied to the COVID-19 vaccine tweet dataset.
Applications:
•	Policy implementations for public awareness.
•	Biotech companies can utilize this analysis to understanding people’s response to vaccination for future vaccine rollouts. 
•	Social media monitoring.
•	Market research.
The rest of the paper is organized as follows. Prior studies section contains different related works relevant to this research. Description of datasets is present in data section. Modelling section contains methodology and proposed methods. Results are discussed at the end with concluding remarks.


[back to top](#table-of-contents)
## Data Background
For this project, we will be using tweets about the COVID-19 vaccines used in the entire world. Tweets are collected using the tweepy Python package to search Twitter API for the keywords relevant to COVID-19 vaccines. The tweets are about Pfizer/BioNTech, Sinopharm, Sinovac (both Chinese-produced vaccines), Moderna, Oxford/Astrazeneca, Covaxin, and Sputnik V vaccines. 
The tweets dataset contains below columns –
•	Id: 		Total 60.3k values
•	User_name: 	60.3k values ,32.6 unique values
•	User_location: 	13.8k missing values
•	User_description: 4158 missing values
•	User_created: 	user creation date.
•	User_followers:	follower count of user
•	User_friends: 	friends count of user.
•	User_favourites
•	User_verified: 	True-6421, False-53.9k
•	Date: 		Tweet date
•	Text: 		Tweet text, 60.3k tweets
•	Hashtags: 	hashtags
•	Source: 		web-31%, phone-29%
•	Retweets: 	retweet count


[back to top](#table-of-contents)
## Prerequisite
You will need the following applications to execute this project-

* Python 3 (or Anaconda distribution with Python 3)
* Jupyter or any other notebook
* TensorFlow, Keras,WorkCloud and other packages that were added in code.

[back to top](#table-of-contents)

## Project Status
We were able to classify tweet sentiment with good accuracy. \
[back to top](#table-of-contents)

## Versioning
Git is used for project versioning. \
[back to top](#table-of-contents)

## Authors
Shani Kumar \
[back to top](#table-of-contents)

## Acknowledgement
It’s been a long timeframe of sickness, sadness, hopelessness, and distress, but the rollout of COVID-19 vaccination globally has given rise to feelings of relaxation for so many. The information about vaccination, side effects, and efficiency is ongoing and circulating on social platforms. This project utilized the power of NLP on Twitter data to understand the sentiments of people over-vaccination. Python package NLTK was used for tokenization/detokenization. LSTM, Bi-LSTM, and 1D CNN models were trained and evaluated for accuracy. Highest accuracy of 72.7% was achieved by Bi-LSTM and it was used for implementation on COVID-19 vaccine tweets dataset. Trends of different sentiments were drawn using Tableau. We see higher number of negative tweets as compared to positive tweets. Moderna, Sinovac, Sputnik, and Johnson & Johnson show an increasing trend in negative sentiment. Pfizer seems to have a constant level of negative sentiment. USA has highest number of vaccinations done as of May 1st. As the 2nd wave of virus has hit India hard, it needs to ramp up its vaccination per hundred. For further analysis dataset with complete tweet text, if available, can be utilized. \
[back to top](#table-of-contents)

## Reference
1.	COVID-19 World Vaccination Progress. (2021, April 17). Kaggle. https://www.kaggle.com/gpreda/covid-world-vaccination-progress
2.	O. (2021). owid/covid-19-data. GitHub. https://github.com/owid/covid-19-data
3.	Staff, A. (2021). A Timeline of COVID-19 Vaccine Developments in 2021. AJMC. https://www.ajmc.com/view/a-timeline-of-covid-19-vaccine-developments-in-2021

[back to top](#table-of-contents)
