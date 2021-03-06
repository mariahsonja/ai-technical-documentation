### Natural Language Processing

Current approaches to NLP are based on deep learning, a subgroup of AI that examines and uses patterns  in  data  to  improve  a  program's  understanding.  There  are  two  main  algorithms  used  to solve NLP problems:

- **Rule-based approach:** Grammatical rules created by experts in linguistics, or knowledge engineers.
- **Machine learning algorithms:** Machine learning models based on statistical methods to perform tasks after being fed examples (training data).

### Benefits of NLP
- Improves accuracy and efficiency when processing documentation.
- It has ability to read, classify, summarize, generate text, translate, extract information and sentiment from texts.

### NLP Process Flow

- **Data Analysis**
- **Data Processing:** converting capital letters to lower case, reorganizing columns, splitting columns, removing unnecessary rows and columns, and splitting columns.
- **Tokenization:** splitting a phrase, sentence, paragraph, or an entire text document into smaller units, such as individual words or terms.
  - *Bigrams:* Tokensconsist of two consecutive words known as bigrams.
  - *Trigrams:* Tokens consist of three consecutive words known as trigrams.
  - *Ngrams:* Tokens consist of ’N’ number of consecutive words known as ngrams

- **Remove Stop Words and Punctuation**
- **Stemming:** removing the suffix from a word and reduce it to its root word(actually -actual).
- **Lemmatization:** it considers morphological analysis of the words and returns meaningful word in proper form–dictionary root.
- **POS(Parts  of  Speech) Tagging:**  it  is about  grammatical  information  of  words  of  the sentence by assigning specific token (Determiner, noun, adjective, adverb, verb, Personal Pronoun etc.) as tag (DT,NN,JJ,RB,VB,PRP,etc.) to each word. A word can have more than one POS depending upon context where it is used. *The (DT)* *Pink (NN)* *Sweater (NN)*.

- **Name Entity Recognition** 

- **Chunking:**  It is  the  process  of  making  a  group  of  tokens  into  chunks.  In  simple  words chunking  is  used  as  selecting  the  subsets  of  tokens.  The  parts  of  speech  are  combined with regular expressions.
- **Bag  of  Words(BOW):** The  bag-of-words  model  is  method  of  feature  extraction  which preprocess the text by converting it into numeric format also known as vectors. **BOW** keeps count of the total occurrences of most frequently used words.
- **TF-IDF(term  frequency–inverse  document  frequency):**  It is  a  numerical  statistic  that  is intended to reflect how important a word is to a document in a collection or corpus.
  - **Term Frequency:** is a scoring of the frequency of the word in the current document.
  - **Inverse  Document  Frequency:**  is  a  scoring  of  how  rare  the  word  is  across documents.


**Reference:** https://medium.com/@jeevanchavan143/nlp-tokenization-stemming-lemmatization-bag-of-words-tf-idf-pos-7650f83c60be 
