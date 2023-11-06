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
