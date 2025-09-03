# Analyzing-customer-review-with-NLP

## About the project
The project aim to take advantage of Natural Language Processing capability of Python libraries (e.g., sklearn, nltk, gensim). It uses data on customer reviews about several theme parks of a fictional company, which amounts to 35,000+ examples. Due its limited scope, the coding of the entire project will be done in a single .ipynb file only. This would include all the steps in a linear manner.

 
<img width="1361" height="321" alt="workflow" src="https://github.com/user-attachments/assets/d3ee2427-565f-4667-9581-2b93443f6ba5" />

Although not entirely related, some Exploratory Data Analysis was also performed. Such analysis extracts extra value from the dataset as well as possibly adding context to result of the machine learning models in later stages.

## The problem
As a well-known theme park brand, company A hold itself in extremely high standard in terms of service quality and customer experience. The company gathered much success in its early days with its customer-centric approach and has been growing continuously since its beginning. However, as the company reaches global scale, it finds harder and harder to impose a consistent quality level of service and to figure out how to improve customer experience. Particularly, the company is drowned in a flood of customer feedback that overwhelmed its best attempts to consume them in traditional way. In light of problem, the company decided to employ data analytics and machine learning capabilities to help it nagivate the sentiments of its global customer base.

## The dataset
The company provided a dataset of 35,000+ customer reviews. The subjects of the reviews are theme park branches in various major cities like California, Hong Kong, and Paris. Along with the reviews themselves, the dataset also include the time and location of the reviews. The below table shows detail (before data cleaning) of the dataset.

|Variable|Data type|Description|
|---|---|---|
|Review_ID |int64| Unique identifier assigning to unique instances of customer review|
|Year_Month|object|The date on which the reviews were made|
|Reviewer_Location|object|The location from where the reviews were made|
|Review_Text|object|The content of the reviews|
|Branch|object|The branch to which the reviews refer|           

## The approach
To consume such large dataset, Python and its relevant libraries will be used. A snapshot of the libraries used in the project can be seen below.

 
<img width="851" height="728" alt="snapshot" src="https://github.com/user-attachments/assets/3d883bc4-9bbe-4945-a934-0296946ff3ec" />


The analysis will include an Exploratory Data Analysis phase to uncover intersing patterns or trends within the dataset. Following that, some Natural Language Processing (NLP) techniques will be used to aggregate the information contained within the reviews. The end goal would be to give a consumable, high-level view on what customers are talking about the theme parks as well as their sentiments on important aspects.

## The development process
After some data cleaning and EDA phase, the development process started with general sentiment analysis on each theme park. This step uses the Natural Language Tool Kit of Python (NLTK). It then devlved deeper and looked specifically at 'service' at each theme park, narrowing down the scope of the topic of interest. At this stage, it looks only at if the sentiment is positive or negative in nature.

Next, topic modeling was addressed. It started with some pre-processing procedures (e.g., stemming, removing stop words, tokenization). Once again, the NLTK library is employed.

To narrow down the topics, a document term was produced using sklearn library and a bar chart of 50 most frequently seen words was made. (see chart in **The result**)

Finally, a LDA model was developed using sklearn library. The products were 10 word clouds representing not only the most popular topics among customer reviews but also the sentiments about them.

Some experiments were done after that in attempt to improve coherence scores of the model but no changes were made to the final model as no significant improvement were observed.

## The result

The first result of the analysis is a general view in sentiment on different branches of the company. From the analysis, it can be seen that customers have the most positive view on Hong Kong branch, California branch, and Paris branch respectively. The gap in sentiment between Paris branch and the other two only eexacerbates when looking specifically at "service" as a topic.

 <img width="747" height="562" alt="image 1" src="https://github.com/user-attachments/assets/a241ba29-54df-4ff5-8ef2-d159e292a876" />


 <img width="616" height="448" alt="image 2" src="https://github.com/user-attachments/assets/e45e8c0e-3a13-4dee-988d-92b5e14d065b" />
 

Following that direction, a list of 50 most common words was generated and visualized into the below bar chart. The chart showed a strong difference between the top 5 words and the rest which have a rather uniform distribution.

 <img width="911" height="353" alt="image 3" src="https://github.com/user-attachments/assets/b299261d-73b9-4503-80a1-a81bf9df018d" />

 

To add more coherence and deep understanding of the data, the words are arranged into word clouds of different topics as below. Each word cloud represent a common topic in reviews.

 
<img width="921" height="453" alt="image 4" src="https://github.com/user-attachments/assets/0e8655fd-2dfd-498c-86bc-fc2db1f1c299" />


A preliminary explanation of these topics:
Topic 1: Having mentioned various themes at theme parks, this topic is likely about most popular themes. With 'like' as one of the keywords, it could indicate positive sentiment.

Topic 2: This topic refers to long waiting lines and crowdedness at the parks.

Topic 3: This word clous is likely to refer to the fastpass at the parks. These allow people to bypass the waiting line, which can easily spark interest in visitors.

Topic 4: This topic is generally positive. It associates this sentiment with firework, parade, and christmas.

Topic 5: This topic is about the characters at the parks. It also shows a liking tone and the favourite activity with the characters.

Topic 6: This topic is likely about people comparing the Paris park with others as 'pari' and a lot of comparison word were included.

Topic 7: This word cloud mainly again emphasizes the people working at the parks.

Topic 8: This topic again talk about the queueing at the parks and adds 'hotel' and 'food' as highly associated words.

Topic 9: This topic reiterates topic 4, talking about the shows, firework and parade. However, it also mentions the long waiting time to these attractions.

Topic 10: This topic shows popularity of the staff and the food quality at the parks.

To add in severity or popularity of these topics, bar charts showing topic popularity were also generated.

 <img width="654" height="397" alt="image 5" src="https://github.com/user-attachments/assets/d220da0c-5a47-4114-b882-a16211799e18" />

 
The bar charts help greatly in determining how serious a topic is among customers as well as zeroing in the biggest topics at any particular branch.

 <img width="773" height="566" alt="image 6" src="https://github.com/user-attachments/assets/e0dc90a1-815d-4094-bf34-61db128346ed" />


To imrove on the result, some experimentations were also done to fine tune hyperparameters, particularly the number of topics. An operation that calculate coherence score when number of topics goes from 1 to 10 was initated. The result is captured in the below chart.


<img width="636" height="463" alt="image 7" src="https://github.com/user-attachments/assets/94fea7c6-c13c-4af4-bc17-f265d2c7d146" />

 
As there is not much significant between 10 topics and the best number of topic in terms of coherence score, development effort will stop here.
