# Analyzing-customer-review-with-NLP

## About the project
The project aim to take advantage of Natural Language Processing capability of Python libraries (e.g., sklearn, nltk, gensim). It uses data on customer reviews about several theme parks of a fictional company, which amounts to 35,000+ examples. Due its limited scope, the coding of the entire project will be done in a single .ipynb file only. This would include all the steps in a linear manner.

(Add workflow)

Although not entirely related, some Exploratory Data Analysis was also performed. Such analysis extracts extra value from the dataset as well as possibly adding context to result of the machine learning models in later stages.

## The problem
As well-known theme park brand, company A hold itself in extremely high standard in terms of service quality and customer experience. The company gathered much success in its early days with its customer-centric approach and has been growing continuously since its beginning. However, as the company reaches global scale, it finds harder and harder to impose a consistent quality level of service and to figure out how to improve customer experience. Particularly, the company is drowned in a flood of customer feedback that overwhelmed its best attempts to consume them in traditional way. In light of problem, the company decided to employ data analytics and machine learning capabilities to help it nagivate the sentiments of its global customer base.

## The dataset
The company provided a dataset of 35,000+ customer reviews. The subjects of the reviews are theme park branches in various major cities like California, Hong Kong, and Paris. Along with the reviews themselves, the dataset also include the time and location of the reviews.

(add table detailing dataframe provided)


## The approach
To consume such large dataset, Python and its relevant libraries will be used.
(add table detailing libraries used)

The analysis will include an Exploratory Data Analysis phase to uncover intersing patterns or trends within the dataset. Following that, some Natural Language Processing (NLP) techniques will be used to aggregate the information contained within the reviews. The end goal would be to give a consumable, high-level view on what customers are talking about the theme parks as well as their sentiments on important aspects.

## The development process
After some data cleaning and EDA phase, the development process started with general sentiment analysis on each theme park. This step uses the Natural Language Tool Kit of Python (NLTK). It then devlved deeper and looked specifically at 'service' at each theme park, narrowing down the scope of the topic of interest. At this stage, it looks only at if the sentiment is positive or negative in nature.

Next, topic modeling was addressed. It started with some pre-processing procedures (e.g., stemming, removing stop words, tokenization). Once again, the NLTK library is employed.

To narrow down the topics, a document term was produced using sklearn library and a bar chart of 50 most frequently seen words was made.
(add chart)

Finally, a LDA model was developed using sklearn library. The products were 10 word clouds representing not only the most popular topics among customer reviews but also the sentiments about them.

Some experiments were done after that in attempt to improve coherence scores of the model but no changes were made to the final model as no significant improvement were observed.

## Major findings after analysis

The proposed approach revealed some major findings using after being used on given data. For example, via data visualization (section 2.1), it was revealed that for the California theme park sees mostly United Stated visitors and Paris park sees mostly United Kingdom traffice while Hong Kong branch has a more balanced traffic. Sentiment analysis (section 4.1 and 4.2) revealed significant drop in sentiment at the Paris theme park, especially in terms of 'services'. Topic modelling (section 5.1 to 5.4) pointed out the most popular likes and dislikes of visitors over a 5 year period. These insights could help the client significantly in deciding their marketing and operational strategies to maximize performance of the parks and improve sentiment of customers toward them.
