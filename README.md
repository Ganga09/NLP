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



