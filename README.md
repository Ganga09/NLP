# NLP
Natural Language processing :
Natural language processing (NLP) is a machine-learning technology that allows computers to interpret, manipulate, and comprehend human language.

## Preprocessing Steps:

### 1. Remove stop words: abt 170<
### 2. Convert into lower cases
### 3. Lemmatization or stemming: find root word of a word and shorten the word:
Stemming:
* reached---> reach
* eating---> eat

but not applicable for:
* thought---> think
* bought----> buy

Lemmatization uses algorithm to find the root word.

### 4. Tokenization:
split the sentences into word by word data.
those are called tokens.
* Not a Good company:
> tokens:
  * Not
  * a
  * Good
  * company

split using space

N-gram:
* The Sun rises in the East
> tokens:1 grm

  *  The
  *  Sun
  *  rises
  *  in
  *  the
  *  East

  > tokens:2 grm

    *  The Sun
    *  Sun rises
    *  rises in
    *  in the
    *  the East

  > tokens:3 grm

    * The Sun rises
    * Sun rises in
    * rises in the
    * in the East

### 5. Vectorization:
 convert tokens to numerical words
 * TF-IDF: Term Frequency-Inverse Document Frequency
> Earth is the third planet from the sun

  > Jupiter is the largest planet




### Demo

####  nltk : natural language tool kit

#nltk: natural language tool kit
#list comprehension:  Syntax: newList = [ expression(element) for element in oldList if condition ]

import nltk

help(nltk)

* ####  Stop words (179)

# ................idetification of stop words.............................
nltk.download('stopwords')                   # download resource for stopwords
from nltk.corpus import stopwords
data=stopwords.words('english')
print(data)


len(data)

* ####   Tokenization

#.......................... word by word data.................................
nltk.download('punkt')                   # download resource punkt ffor tokenization
s1='Luminr technolab is located at Kakkanad'
from nltk.tokenize import word_tokenize
token=word_tokenize(s1)
print(token)

sentence='''The Natural Language Toolkit(NLTK) is an open source python library for natural language processing. a free online book is avaiable'''
token=word_tokenize(sentence)
print(token)

* #### Demo1

remove stop words and print the tokens

import nltk
nltk.download('stopwords')
nltk.download('punkt')
from nltk.corpus import stopwords
data=stopwords.words('english')
from nltk.tokenize import word_tokenize
sentence='''The Natural Language Toolkit(NLTK) is an open source python library for natural language processing. A free online book is avaiable'''
token=word_tokenize(sentence)
result=[i for i in token if i.lower() not in data] # from token tokens if tokens not present in data
print(result)


#### Ngrams

from nltk.util import ngrams
sen='this is a very good book to study'
data= ngrams(sequence=nltk.word_tokenize(sen),n=1)
for i in data:
  print(i)

Stemming:
1. Porter stemmer
2. Snowball stemmer


from nltk.stem import PorterStemmer
from nltk.tokenize import word_tokenize
ps=PorterStemmer()
words=['programs','programming','walking','jumped','reached','catching','removed']
for i in words:
  print(i,":",ps.stem(i))

from nltk.stem import SnowballStemmer
ss=SnowballStemmer('english')
for i in words:
  print(i,":",ss.stem(i))

Lemmatization

from nltk.stem import WordNetLemmatizer
nltk.download('wordnet')
nltk.download('omw-1.4')
wlem=WordNetLemmatizer()
print("rocks:",wlem.lemmatize('rocks'))

#ing :stemming
#s: lemmatization

remove character

#regular expression
str1='Wonderful%% @Peacock!122234$'
import re
str2=re.sub('[a-z]', ' ',str1)
print(str2) # replaces all small letters with space' '
str3=re.sub('[a-zA-Z0-9]',' ',str1)# [a-z][A-Z][0-9]
str3
