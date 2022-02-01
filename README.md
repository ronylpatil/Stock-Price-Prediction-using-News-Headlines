<h2 align="center">
Stock Sentiment Analysis using News Headlines

<h4 align="center">
  
<b>Here we will discuss a complete End to End approach for building Stock Sentiment Analysis using News Headlines</b>
</h4></h2>
  
<p align="center">
  <img class="center" src ="https://github.com/ronylpatil/Stock-Sentiment-Analysis-using-News-Headlines/blob/main/stock.png" alt="Drawing" style="width: 950px; height: 400px">
</p>

#### What is NLP(Natural Language Processsing)?
It is basically subset of Linguistic(Human Languages), Computer Science, and Artifical Intelligence. Here we will programe our machines in a such a way that it can understand, interpreat, and manipulate human languages.

<p align="center">
  <img class="center" src ="https://github.com/ronylpatil/Stock-Sentiment-Analysis-using-News-Headlines/blob/main/nlp1.png" alt="Drawing" style="width: 1300px; height: 425px">
</p>

#### What is Natual Language?
As we all know that in the beginning of the era humans were also animals but humans findout a way to communicate with each other and over a time it start improving and then it becomes a language. As it is evolve naturally over a time, it known as Natural Language. Natural Language can be speech or signs. It is different from artificial languages such as python, java...

#### Real World Application of NLP : <b>
- Contextual Advertisement(Target Add.)
- Social Media - </b>Removing adult content, opinion minning.
- <b>Search Engine -</b> From last 10 to 15 years google search engine evolved alot. Now you need to just ask question, google will quickly featch result in single line.
- <b>Chatbots</b>

<h3 align="center">
  Complete NLP Pipeline for Stock Sentiment Analysis
</h3>

<b>Problem Statement - </b> We need to build a model that helps the investors to avoid risk and financial crises when making investment decision. Here we will predict stock market behaviour whether it will fall or raise. This is basically an attempt to study relationship between news headlines and stock price. 

<b>Here we are considering different types of news related to companies, markets and financial reports.</b>

The NLP Pipelines are set of steps followed to build an end to end NLP projects.
<b>
1. Data Acquisition / Data Collection
2. Text Preprocessing
3. Feature Engineering
4. Modelling and Evalution
5. Deployment 

</b>

<h4 align = "center">
  1. Data Acquisition / Data Collection
</h4>

Data Collection is one of the difficult task in any of the Machine Learning, or Deep Learning projects. Here I have mentioned 3 possible scenarios.
<b>
```
Data Acquisition
  |--- 1. Dataset is readymade available.
        |--- 1. We have readymade dataset in CSV format.
        |--- 2. We have data in database.
             |--- In this case we need to contact with our data engineering team for collecting the data. 
        |--- 3. We have very less data.
             |--- Here we need to do Data Augmentation.
                  |--- 1. We can generate fake data by replacing word's with there synonyms.
                  |--- 2. Bi-gram Flip - We can flip the two words to add some variation to the text.
                  |--- 3. Back Translate - We will first translate the text into different language then again 
                                           re-translate it into original language, it will basically rephrase
                                           the text. 
                  |--- 4. Adding Noise - We can add some noise in the sentence which dont have any meaning.
                                         Here sentiment will be same only sentence will change.
                  
  |--- 2. Data from third party.
       |--- 1. We can use public dataset.
       |--- 2. We can get the data by webscraping.
       |--- 3. We can use API's to get the data.
       |--- 4. Data can be extracted from PDF files, images, or audio files.
        
  |--- 3. We dont have data.
       |--- If we dont have data in this case we need to take survey from our loyal customers and then label them manually. 
            Then we can use heuristic approach to get the data. In such cases we need to use an intelligent approach
            to get the data.

```
</b>

<b>Our Data Collection Approach -</b> Here we will collect headlines of economical news of a company and collect the stock market data according to the timestamp of the given economic news headlines. On the one hand, we will analyze the stock's starting, closing, lowest, and highest prices, while on the other hand, we will analyse the Top-20 to 25 news headlines.


<h4 align = "center">
  2. Data Preprocessing
</h4>

Here we have 3 scenarios.
<b>
```
Data Prepration
    |--- 1. Basic Cleaning
         |--- 1. Using regular expression to remove impurities.
         |--- 2. Unicode Normalization - Here we will encode the emojies so that it will be easily understandable 
                 by our machine.
         |--- 3. Spelling Checking.
        
    |--- 2. Basic Text Preprocessing
         |--- 1. Tokenization - Spliting the text into smaller units.
              |--- 1. Sentence Tokenization.
              |--- 2. Word Tokenization.
              
         |--- 2. Optional Preprocessing Steps
              |--- 1. Removing stopwords - removing words that basically used for sentance formation.
              |--- 2. Text Normalization - It reduce the derivational form of word to its base word.
                   |--- 1. Stemming - It remove the last few characters of words and return the base word. It dont care 
                                      about context.
                   |--- 2. Lemmatization - It is similar as stemming, only difference is it considerd context and convert
                                           the word to meaningfull base form.
              |--- 4. Removing digits, punctuations, and ...
              |--- 5. Lower casing or upper casing the text.
              |--- 6. Language detection.
          
    |--- 3. Adv. Text Preprocessing
         |--- 1. Part of speech tagging.
         |--- 2. Parsing.
         |--- 3. Co-reference Resolution. 
         
```
</b>

<h4 align = "center">
  3. Feature Engineering / Text Representation / Text Vectorization / Text Representation / Feature Extraction
</h4>
Actually dealing with text data is one of the difficult task as compare to image data or audio/speech data because in images we deal with pixels and in speech data we deal with amplitude and frequency so that we can easily get numeric data from it. But in textual data there is no chance! Here we will face various challenges such as suppose anyhow we have converted textual data into numeric data but here we have to also focus that the numeric vector representing the textual data should also convey semantic meaning of the sentence. The hidden meaning of the text should also be convery from the vector, this is our end goal. 

In this stage we will convert the text data into numeric format so that we can easily feed it to Machine Learning Algo. or Deep Learning Arch.  
<b>
```
Feature Engineering Techniques
      |--- 1. One-hot Encoding - Ancient techique, having a lot of drawbacks.
      |--- 2. Bag of Words - It use count freq. of each word.
      |--- 3. N-gram - Similar as BoW.
      |--- 4. Tf-IDF - Use weights for representing each word.
      |--- 5. Custom Features / Handcrafted Features - Generate features based on domain knowledge.
      |--- 6. Word2vec - Deep Learning approach for creating word embeddings.
      ...

```
</b>
Feature Eng. depends on the problem statement, based on problem statement we have to decide the approach.

<h4 align = "center">
  4. Modelling and Evalution
</h4>

We have converted the data into the suitable numeric format, now its time to feed it to algorithm.<b>
```
|--- 1. Modelling - Here we will build model for our problem statement.
            |--- 1. Heuristic Approach
            |--- 2. Machine Learning Approach
                    Mostly used in basic sentiment analysis problem's.
                    |--- Popular ML Algorithms
                            |--- Naive Bayes
                            |--- Logistic Reg.
                            |--- Support Vector Machine
                            |--- Latent Dirichlet Allocation (LDA)
                            |--- Hidden Markov Model (HMM)
                            ...
            |--- 3. Deep Learning Approach
                        |--- 1. Transfer Learning 
                                ex. BERT Model
                        |--- 2. RNN(Recurrent Neural Nertwork)
                                Deal with sequential data. Used in Bot's, alexa, siri, machine translation...
            |--- 4. Cloud API's
                    GCP, Azure, AWS... have sol. of different problems we can directly use their API's.
                    In this case we don't need to use any algorithm, directly hit the api's and use their services. 
        
        Note - Which approach we need to use is depends on 2 things : 
               1. Amount of data. 
               2. Nature of problem statement.
  
|--- 2. Evaluation - Here we will evaluate our model.
        (In Industrial Level projects we need to focus on both the approaches)
            |--- 1. Intrensic Evaluation (Technical Approach)
                        |--- Confusion Matrics
                        |--- Precision
                        |--- Recall
                        |--- Accuracy
                        |--- Classification Report
  
            |--- 2. Extrensic Evaluation (Business Level Approach)
                    Once our model get deployed it becomes product and in such business setting's we evaluate our model.
  
```
</b>


<h4 align = "center">
  5. Deployment
</h4>

The final step...
<b>
```
Deployement Steps
      |--- 1. Deploy
              The deployment steps varies from project to project; for example, if we are developing a
              full-fledged project, our approach will be different, and if we are developing a single feature, our 
              approach will be different.

      |--- 2. Monitor
              Here we will build a dashboard, which will plot graphs of various evaluation metrics such as
              intrensic evaluation & extrensic evaluation.

      |--- 3. Update
              In this stage we will update our model based on our requirement's.
              As our model get new data it get trained on the server. In this case our approach would be little 
              bit different.        

```
</b>

<h4 align = "center">
  6. Challenges - We are just at 5% of the NLP's potential!
</h4>

Actually predicting the behaviour of stock market based on news minning is very attractive field of research and it has a lot of challenges because of unstructured nature of news. Many times, we've seen that news reporters tweak the headlines so smoothly so that we can't tell whether they're blaming or supporting the victim. One punctuation mark has power to change the meaning of the whole sentence. Therefore NLP is very challenging task. Here news minning means extracting hidden, useful and potentially unknown patterns from news data to obtain knowledge. 


<h4 align="center">
  
[![Website](https://img.shields.io/badge/Made%20with-%E2%9D%A4-important?style=for-the-badge&url=https://www.linkedin.com/in/ronylpatil/)](https://www.linkedin.com/in/ronylpatil/)  
</h4>
