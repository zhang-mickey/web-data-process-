```
what probability should a fact have so that it is included in all possible worlds
```
```
Write the name of a popular knowledge base designed to store the meaning of English words
```
```
Which of the following systems can be used for open information extraction?
ReVerb
DIPRE
MALLET
AIDA  
```
# web-data-process
# NLP 
## Tokenization
Given a character sequence, split it into pieces called tokens.  
### strategy
`Split at white spaces and hyphens`   
`NLTK`  
#### problematic input
Tokenization is language-specific  

## Stemming or lemmatization
Goal: reduce inflectional forms to base form
### Lemmatization
Reduction to dictionary headword() form.  
### Stemming
Reduce terms to their root.  

# Information Extraction 
# Entity Recognition(ER)
two types of information extraction  

## Named Entity Recognition
find and classify names in text  
### 3 standard approaches
`Hand-written regular expressions`
`Using classifiers`  
`Sequence models`  
### NeuroNER
uses BILSTM for entity recognition.  
#### Token embedding
Map every character,n-gram,token into a vector of real numbers.  


## Relation Extraction(RE)
# candidate Entity Ranking  
`Context-independent features` :just rely on the surface-form of the entity mention.    
`Context-dependent features` : also look at the context around the entity mention.   
## Context-independent features
### Entity popularity
Given a certain mention, pick the entity which is the most popular.  
## Context-dependent features
The context around the entity offers valuable information.  
### Bag of words(BOW)
It disregards grammar and word order 
### Concept vectors
#### cosine similarity(经典的求相似度方法)

## solve Unlinkable
when none of the candidate entities is suitable  
### Add NIL as a special entity and consider it during the ranking process
If NIL will get the highest score, then the entity is considered unlinkable.  


## Feed-forward network
do not have memory
## Recurrent neural network(RNN)
have memory by adding cycles.   
They are networks with loops in them, allowing information to persist.  
<img width="90" alt="image" src="https://github.com/zhang-mickey/web-data-process-/assets/145342600/d1483367-0f44-41c0-9e10-cba12fd2c1ab">  
<img width="410" alt="image" src="https://github.com/zhang-mickey/web-data-process-/assets/145342600/c183a087-0d25-4720-a85a-425bddb53306">  

### LSTM
Unfortunately, as that gap grows, RNNs become unable to learn to connect the information.  
<img width="286" alt="image" src="https://github.com/zhang-mickey/web-data-process-/assets/145342600/36a8c597-d04d-4fae-92e5-ae95c67acaa4">  
<img width="382" alt="image" src="https://github.com/zhang-mickey/web-data-process-/assets/145342600/e3a6a466-2db3-48da-8996-9f34af3611ff">  
LSTM capable of learning long-term dependencies  
<img width="529" alt="image" src="https://github.com/zhang-mickey/web-data-process-/assets/145342600/cd2dc61f-be53-462c-bd7c-7121e4d4436e">  
<img width="532" alt="image" src="https://github.com/zhang-mickey/web-data-process-/assets/145342600/ea5b5836-39f6-4a12-ba42-cbb1a7e38e80">  
#### Forget layer decide what information we’re going to throw away
<img width="492" alt="image" src="https://github.com/zhang-mickey/web-data-process-/assets/145342600/e62498fc-823f-45d0-a75c-9acb68e1579a">

#### decide what new information we’re going to store 
<img width="520" alt="image" src="https://github.com/zhang-mickey/web-data-process-/assets/145342600/f5888a42-edc7-470f-aebd-1af69d061247">  
<img width="468" alt="image" src="https://github.com/zhang-mickey/web-data-process-/assets/145342600/1457bda8-3f35-41c9-87d7-f196a3669dec">

#### decide what we’re going to output
<img width="502" alt="image" src="https://github.com/zhang-mickey/web-data-process-/assets/145342600/2d69bf1e-ed94-443b-bacc-a60117cdf763">


# WSD(Word Sense Disambiguation)
WSD is a natural classification problem: Given a word and its possible senses, as defined by a dictionary, classify an occurrence of the word in context into one or more of its sense classes. The features of the context (such as neighboring words) provide evidence for classification.  

methods to WSD are classified according to the source of knowledge used in word disambiguation.
## dictionary-based method(use the knowledge encoded in lexical resources)

### Lesk algorithm
## supervised machine learning methods
 classifier is trained for each distinct word on a corpus of manually sense-annotated  
 assume that the context can provide enough evidence on its own to disambiguate the sense    
## semi-supervised Methods
Due to the lack of training corpus, most of the word sense disambiguation algorithms use semi-supervised learning methods.  

### bootstrapping from seed data

# literature
https://web.stanford.edu/~jurafsky/slp3/slides/  
