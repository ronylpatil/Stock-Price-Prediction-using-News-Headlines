<h2 align="center">
Stock Sentiment Analysis using News Headlines

<h4 align="center">
  
[![Website](https://img.shields.io/badge/Made%20with-%E2%9D%A4-important?style=for-the-badge&url=https://www.linkedin.com/in/ronylpatil/)](https://www.linkedin.com/in/ronylpatil/)
  
<b>Here we will discuss a complete End to End approach for building Stock Sentiment Analysis using News Headlines Project.</b>
  
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
As we all know that in the begining of the era humans were also animals but humans findout a way to communicate with each other and over a time it start improving and then it becomes a language. As it is evolve naturally over a time, it known as Natural Language. Natural Language can be speech or signs. It is different from artificial languages such as python, java...

#### Real World Application of NLP : <b>
- Contextual Advertisement(Target Add.)
- Social Media - </b>Removing adult content, opinion minning.
- <b>Search Engine -</b> From last 10 to 15 years google search engine evolved alot. Now you need to just ask question, google will quickly featch result in single line.
- <b>Chatbots</b>

<h3 align="center">
  Complete NLP Pipeline for Stock Sentiment Analysis
</h3>

<b>Problem Statement - </b> We need to build a model that helps the investors to avoid risk and financial crises when making investment decision. Here we will predict stock market behaviour whether it will fall or raise. This is basically an attempt to study relationship between news headlines and stock price. 

The NLP Pipelines are set of steps followed to build an end to end NLP projects.
<b>
1. Data Acquisition / Data Collection
2. Text Preperation
3. Feature Engineering
4. Modelling and Evalution
5. Deployment 

</b>

<h4 align = "center">
  1. Data Acquisition / Data Collection
</h4>

Data Collection is one of the difficult task in any of the Machine Learning, or Deep Learning projects. Here we may have 3 scenerio. First, either <b>readymade dataset</b> will be available, or we can take it from any <b>third party</b>, or <b>we dont have data.</b>
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

<b>Data Collection Technique -</b> Here we will collect headlines of economical news of a company and collect the stock market data according to the timestamp of the given economic news headlines. On the one hand, we will analyze the stock's starting, closing, lowest, and highest prices, while on the other hand, we will analyse the Top-20 to 25 news headlines.


<h4 align = "center">
  2. Data Preperation
</h4>




























