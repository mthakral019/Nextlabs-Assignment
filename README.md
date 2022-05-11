# Nextlabs-Assignment
Part-1

Question1:
Write a regex to extract all the numbers with orange color background from the below text in italics. data={"orders":[{"id":1},{"id":2},{"id":3},{"id":4},{"id":5},{"id":6},{"id":7},{"id":8},{"id":9},{"id":10},{"id":11},{"id":648},{"id":649},{"id":650},{"id":651},{"id":652},{"id":653}],"errors":[{"code":3,"message":"[PHP Warning #2] count(): Parameter must be an array or an object that implements Countable (153)"}]}

Answer 1:re.findall(r"[^#|\(\d+]\d+",str(data)).Check my complete answer at https://github.com/mthakral019/Nextlabs-Assignment/tree/main/Part%201/Question%201

Question-2:
Here’s the list of reviews of Chrome apps - scraped from Playstore.  DataSet Link
Problem statement - There are times when a user writes Good, Nice App or any other positive text, in the review and gives 1-star rating. Your goal is to identify the reviews where the semantics of review text does not match rating. Your goal is to identify such ratings where review text is good, but rating is negative- so that the support team can point this to users. 

Answer 2: After understanding the problem statement It was very clear that it's an NLP problem where we need to find the sentiments of reviews individually and find out those reviews where sentiment is positive but the ratings given out of 5 is poor. So first of all my main task was to find out the sentiment of a review and to that I have used SentimentIntensityAnalyzer which comes with nltk library. The reason for using this Sentiment Analyzer was that it gives most appropriate results on real-life used language. So After finding out the Sentiments of text reviews we find out those reviews where sentiment score says that review is positive but the ratings were poor. I used Flask to deploy this model where it shows the mismatched reviews and ratings. Check my complete answer at https://github.com/mthakral019/Nextlabs-Assignment/tree/main/Part%201/Question%202/chrome_rating

Question-3:
Ranking Data - Understanding the co-relation between keyword rankings with description or any other attribute. Here’s the dataset. 
Suggested questions:
1.Is there any co-relation between short description, long description and ranking? Does the placement of keyword (for example - using a keyword in the first 10 words - have any co-relation with the ranking)?
2.Does APP ID (Also known as package name) play any role in ranking?  
3.Any other pattern or good questions that you can think of and answer?

Answer 3: It was an interesting question here I did the EDA which tries to answer these questions. Check my complete answer at https://github.com/mthakral019/Nextlabs-Assignment/tree/main/Part%201/Question%203


Part-2

Question 1:Check if the sentence is Grammatically correct: Please use any pre-trained model or use text from open datasets. Once done, please evaluate the English Grammar in the text column of the below dataset. 

Answer 1: Honestly It was the most tough question out of all. To solve this question I have used BERT. BERT(Bidirectional Encoder Representations from Transformers) is a transformer-based machine learning technique for natural language processing pre-training developed by Google. To train our BERT model we used The Corpus of Linguistic Acceptability (CoLA) dataset for single sentence classification. It's a set of sentences labeled as grammatically correct or incorrect.I first trained the model using the above mentioned data and saved this trained model. So that we can use it later by importing directly. I did all these steps in this notebook:https://github.com/mthakral019/Nextlabs-Assignment/blob/main/Part%202/Question%201/Grammar%20Classifier/saved_model-20220510T081104Z-001/saved_model/BERT/Grammar_checker.ipynb 
Later I used this trained model and imported it to classify texts in our dataset which I did here :https://github.com/mthakral019/Nextlabs-Assignment/blob/main/Part%202/Question%201/Grammar%20Classifier/saved_model-20220510T081104Z-001/saved_model/BERT/Grammar_checker.ipynb
Finally I was able to classify all the rows in my dataset as gramatically-correct or gramatically-incorrect.

Question-2:Write about any difficult problem that you solved. (According to us difficult - is something which 90% of people would have only 10% probability in getting a similarly good solution.

Answer 2: I have worked on KPI (Key Performance Indicator) Problem where my goal was to create a model/system where an individual was getting evaluated automatically without the bias of any Manager/Leadership. I was able to achieve the goal. I used the classification method to classify if an employee is above average or below average based on their performance. This system was so helpful that the Leadership started using it for providing the appraisals or PDE to employees based on their work performances.

Question-3:Formally, a vector space V' is a subspace of a vector space V if
V' is a vector space
every element of V′ is also an element of V.
Note that ordered pairs of real numbers (a,b) a,b∈R form a vector space V. Which of the following is a subspace of V?
The set of pairs (a, a + 1) for all real a
The set of pairs (a, b) for all real a ≥ b
The set of pairs (a, 2a) for all real a
The set of pairs (a, b) for all non-negative real a,b
 
 Answer 3: Since V (a,b) is a vector space where a,b ∈ R. So all the set of pairs (a,b) where a,b are non-negative real a,b will lie inside vector space V. Hence Option 4 is right
