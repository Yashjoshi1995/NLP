# NLP
1. Cleaning text data.ipynb:
Usually we will be having a raw text which need to be cleaned and preprocessed before fitting a model to it.
Pre-processing text data
Cleaning up the text data is necessary to highlight attributes that you're going to want your machine learning system to pick up on. Cleaning (or pre-processing) the data typically consists of a number of steps:

a. Remove extra spaces
b. Remove punctuation
c. Case normalization: Converting all charachters to either lower case or upper case
d. Tokenization: Splitting a sentence into words and creating a list, ie each sentence is a list of words
e. Remove stopwords
f. Lemmatize/Stem: Getting words to its root form. In preprocessing either Stemming or Lemmatizing is done.

2. For fitting a model, the text must be converted to numeric form which can be understood by the machine. This is called as Vectorization. There are different methods by which we can perform this:
  a. Bag of words(BOW): In this all the unique words are collected from the corpus(text data) and the frequency of each word in each sentence is taken(called as Term Frequency(TF)). This is done by CountVectorizer of nltk library. In this, we can give parameter(ngram_range) to set how many words we want to have, ie:;
    unigram - a token comprises of exactle one word
    bigram: a token comprises of exactly 2 words
    trigram: a token comprises of exactly 3 words
    The output we get from this is called as 'Document Term Matrix'.
   BOW will not give weightage to more important words. It simply gives the frequency. For large datasets it is not used.
   
   b. Term Frequency-Inverse Document Frequency(TF-IDF): It is used to give weightage or importance to uncommon words or seldom used words.
   
  Both BOW and TF-IDF doen't store the semantic information.
