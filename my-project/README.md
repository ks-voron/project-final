<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# App-Review-Classifier
*[Kseniya Voronkova]*

*[Data Analytics Part Time Course, Barcelona September 2021]*

## Content
- [Project Description](#project-description)
- [Hypotheses / Questions](#hypotheses-questions)
- [Dataset](#dataset)
- [Cleaning](#cleaning)
- [Analysis](#analysis)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Workflow](#workflow)
- [Organization](#organization)
- [Links](#links)

## Project Description
Unstructured data in the form of text is present everywhere today. Text can be a rich source of information, but due to its unstructured nature it can be hard to extract insights from it. Text classification is one of the important task in machine learning (ML). It is a process of assigning categories to documents helping us to automatically & quickly structure and analyze text in a cost-effective manner. 

## Hypotheses / Questions 
Using capabilities of NLP, find an automated approach to the classification of user reviews to improve the efficiency and customer satisfaction.

## Dataset
* Reviews extracted from Google Play Store (Android). Filtered to reviews with rating less than 4 and translated to English. 

## Cleaning
Before we move to model building, we need to preprocess our dataset:

1. Removing punctuations, special characters, URLs & hashtags
2. Stop-word removal: We can remove a list of generic stop words from the English vocabulary using nltk. A few such words are ‘i’,’you’,’a’,’the’,’he’,’which’ etc.
3. Stemming: Refers to the process of slicing the end or the beginning of words with the intention of removing affixes(prefix/suffix)

It’s difficult to work with text data while building Machine learning models since these models need well-defined numerical data. The process to convert text data into numerical data/vector, is called vectorization or in the NLP world, word embedding. Bag-of-Words(BoW) and Word Embedding (with Word2Vec) are two well-known methods for converting text data to numerical data.

## LSA (Bag of Words model)
There are a few versions of Bag of Words, corresponding to different words scoring methods. We use the Sklearn library to calculate the BoW numerical values using these approaches:

1. Count vectors: It builds a vocabulary from a corpus of documents and counts how many times the words appear in each document
2. Term Frequency-Inverse Document Frequencies (tf-Idf): Count vectors might not be the best representation for converting text data to numerical data. So, instead of simple counting, we can also use an advanced variant of the Bag-of-Words that uses the term frequency–inverse document frequency (or Tf-Idf). Basically, the value of a word increases proportionally to count in the document, but it is inversely proportional to the frequency of the word in the corpus

## Word2Vec model
One of the major drawbacks of using Bag-of-words techniques is that it can’t capture the meaning or relation of the words from vectors. Word2Vec is one of the most popular technique to learn word embeddings using shallow neural network. 
We'll be using the pre-trained vectors trained on part of Google News dataset (about 100 billion words). The model contains 300-dimensional vectors for 3 million words and phrases.


## Conclusion
* Used different methods when converting textual data to numerical. 
* Visualization of the results.
* The clusters are not well distinguished due to small amounts of data and to the fact that the majority of the reviews have the same topic.

## Future Work
* Obtain larger dataset.
* Try out other model (Latent Dirichlet Allocation (LDA)).

## Workflow
1. Importing Libraries
2. Loading the data set & EDA
3. Text pre-processing
4. LSA
5. Word2Vec
6. Conclusions

## Links

[Repository](https://github.com/ks-voron/project-final/)  
[Slides](https://docs.google.com/presentation/d/1bxg1m4SUxHHR_AfDG0EDk3ewB9sdF4Yf/edit?usp=sharing&ouid=115060573278927714485&rtpof=true&sd=true)   
