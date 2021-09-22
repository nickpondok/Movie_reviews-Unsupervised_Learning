### Abstract

The goal of this project was to generate a topic model that informs Disney about which topis are being discussed about their new movie. I worked with data scraped from google reviews and then used NLP in order to generate my topic model. I then used that topic model to do some EDA to help draw conclusions to answer Disney's questions

### Design
The goal of this project was to take a close look at audience reviews of Marvel's new movie Shang-Chi. Disney wants to know what audiences are talking about when it comes to the movie. They want to know what topics are being talked about in a negative light and which ones are being talked about in a positive light. My goal was to generate a topic model that addressed these questions.

### Data

The data set consisted of 2,206 audience movies reviews from google reviews. The reviews needed to be spell checked, lemmatized, and stop words and punctuation needed to be removed. Additionally I compounded the title of the move and actor/actresses names. The data was then ran through a countvectorizer with unigrams and a max_df of 0.8. First an NMF model was created, but it did not generate significant topics, however some words from this model did stick out and I decided to try and hone in on those words by using a corex model with anchor words. This helped generate more significant topics: Action sequences, plot, cast, Asian culture. The polority and topic correlation for each document was calculated and each document was assigned a topic by taking the topic with the maximum correlation. I then took a look at the distribution of topics amongst both positive a negative reviews to draw my conclusions. 

### Algorithms
1) NMF model was used to generate top words for 4 different topics. These words helped influence my anchor words for my corex model. 

2) Corex Model was created using anchor words 'story','culture','martial','cast'
    Polarity was used to assign positive or negative sentiment and Topic correlation was used to assign topics to documents 
    
### Tools 
Beautiful soup and selenium for webscraping 
NLTK, Textblob, Spacy all used for preprocessing 
matplotlib for visualizations 
NMF and Corex for topic modeling 
