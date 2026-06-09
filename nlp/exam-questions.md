# NLP Exam Questions Bank by Yana Siao

## Text Classification

### **Q1.** The main reason for performing stemming before building a text classifier is to:
- a. correct misspellings in the text
- b. to lowercase the text
- c. NONE of the other options are correct
- d. concentrate representation around STEM (Science Technology Engineering and Mathematics) terms only
- e. reduce the feature set while increasing the number of examples of each token
- f. to split overly long words into sequences of shorter words
- g. increase the feature set while decreasing the number of examples of each token

### **Q2.** Which deep learning model has been widely used for NLP tasks, in particular for learning text classifiers?
- a. NONE of the other answers is correct
- b. K-means
- c. DeepText
- d. Support Vector Machines
- e. ResNet-152
- f. BERT
- g. Decision trees
- h. Naive Bayes
- i. YOLO

### **Q3.** If the output of a text classifier produces the following confusion matrix on the test set:
| | Predicted + | Predicted − |
|---|---|---|
| Actual + | 95 | 25 |
| Actual − | 5 | 75 |

What is the Precision of the classifier?
- a. 85%
- b. 79.2%
- c. 93.8%
- d. 75%
- e. 47.5%
- f. 90%
- g. NONE of the other options is correct
- h. 95%

### **Q4.** If the output of a text classifier produces the following confusion matrix on the test set:
| | Predicted + | Predicted − |
|---|---|---|
| Actual + | 75 | 5 |
| Actual − | 25 | 95 |

What is the Precision of the classifier (for the positive class)?
- a. 79.2%
- b. NONE of the other options is correct
- c. 93.8%
- d. 90%
- e. 47.5%
- f. 95%
- g. 85%
- h. 75%
  
### **Q5.** Imagine you are building a Naive Bayes classifier for detecting spam emails. You have 2,000 spam emails and 8,000 not-spam emails. What is the PRIOR probability of seeing a spam email?
| | 'win' | 'drugs' | 'cheap' | 'wow' | 'prof' | 'greatest' | 'exam' | 'prior' |
|---|---|---|---|---|---|---|---|---|
| Spam | 35 | 50 | 54 | 251 | 5 | 31 | 1 | 20 |
| Not-spam | 14 | 9 | 27 | 1501 | 95 | 120 | 57 | 40 |
- a. 0.5%
- b. 20%
- c. 25%
- d. 80%
- e. 1%
- f. NONE of the other options are correct
- g. 10%

### **Q6.** Imagine you are building a Naive Bayes classifier for detecting spam emails. You have 2,000 spam emails and 8,000 not-spam emails. What is the LIKELIHOOD probability P('win'|Spam)?
| | 'win' | 'drugs' | 'cheap' | 'wow' | 'prof' | 'greatest' | 'exam' | 'prior' |
|---|---|---|---|---|---|---|---|---|
| Spam | 35 | 50 | 54 | 251 | 5 | 31 | 1 | 20 |
| Not-spam | 14 | 9 | 27 | 1501 | 95 | 120 | 57 | 38 |
- a. 0.27%
- b. 29%
- c. 66.67%
- d. 12.1%
- e. 5.4%
- f. NONE of the other options are correct
- g. 3.5%

### **Q7.** Imagine you are building a Naive Bayes classifier for detecting spam emails. You have 2,000 spam emails and 8,000 not-spam emails. What is the LIKELIHOOD probability P('win'|Not-spam)?
| | 'win' | 'drugs' | 'cheap' | 'wow' | 'prof' | 'greatest' | 'exam' | 'ever' |
|---|---|---|---|---|---|---|---|---|
| Spam | 35 | 50 | 54 | 251 | 5 | 31 | 1 | 20 |
| Not-spam | 14 | 9 | 27 | 1501 | 95 | 120 | 57 | 38 |
- a. 0.27%
- b. 29%
- c. 66.67%
- d. 12.1%
- e. 5.4%
- f. NONE of the other options are correct
- g. 3.5%

### **Q8.** Consider a Naive Bayes (NB) model for predicting whether a student gets a good grade based on her describing the exam as "easy" but "long". With: P("easy"|good)=2/3, P("long"|good)=1/3, P("easy"|bad)=1/3, P("long"|bad)=2/3, P(good)=3/4. What is the probability that a student gets a good grade given that she describes the exam as "easy" but "long"?
- a. 1/3
- b. 2/3
- c. NONE of the other options are correct
- d. 1/2
- e. 3/4
- f. 1/4

### **Q141.** Consider a Naive Bayes (NB) model for predicting whether a student gets a good grade based on her describing the exam as "easy" but "long". With: P("easy"|good)=2/3, P("long"|good)=1/3, P("easy"|bad)=1/3, P("long"|bad)=2/3, P(good)=3/4. What is the denominator value (marginal probability of the evidence P("easy","long")) used to compute the posterior?
- a. 2/9
- b. 5/18
- c. NONE of the other options are correct
- d. 7/24
- e. 1/6
- f. 1/4

### **Q142.** Consider a Naive Bayes (NB) model for predicting whether an email is spam based on the presence of words. Given: P("win"|spam)=4/10, P("win"|not-spam)=1/10, P(spam)=2/10. What is the denominator value (marginal probability of the evidence P("win")) used to compute the posterior?
- a. 2/10
- b. 4/10
- c. 1/10
- d. NONE of the other options are correct
- e. 16/100


### **Q9.** Consider a Naive Bayes (NB) model for predicting whether an email is spam based on the presence of words. Given: P("win"|spam)=4/10, P("win"|not-spam)=1/10, P(spam)=2/10. What is the probability that an email containing the word "win" is spam?
- a. 1/2
- b. 4/10
- c. 2/10
- d. 1/10
- e. NONE of the other options are correct

### **Q10.** Which of the following tasks involves assigning a label from a predefined set of categories to a piece of text?
- a. Sentiment analysis
- b. Text summarization
- c. Named entity recognition
- d. Topic modeling
- e. NONE of the other options is correct
- f. Text clustering

### **Q11.** Heaps' law states that:
- a. the frequency of a term in a document is inversely proportional to its rank
- b. NONE of the other answers is correct
- c. the number of transistors on a computer chip doubles approximately every 2 years
- d. the size of the vocabulary grows roughly in proportion to the square root of the length of the document
- e. for every action there must be an equal and opposite reaction
- f. the more interesting the topic of the course, the harder is the exam

### **Q12.** The size of the vocabulary grows roughly in proportion to the square root of the length of the document/collection — this is a statement of whose law?
- a. NONE of the other answers is correct
- b. Mandelbrot's law
- c. Murphy's law
- d. Heap's law
- e. Moore's law
- f. Zipf's law

### **Q13.** Zipf's law states that:
- a. the frequency of a term in a document collection is inversely proportional to its rank
- b. the number of parameters in a neural network grows exponentially with time
- c. vocabulary size grows as a function of document length
- d. language models are inherently unstable
- e. NONE of the other answers is correct

---

## Text Search & Clustering

### **Q14.** You are building a document search system and train a BERT model to classify whether a document is relevant to a user query. How might you reduce the computational burden when deploying this system without greatly degrading performance?
- a. By using GPT2 rather than BERT to classify the documents
- b. By using a lexical or semantic search engine to first find a set of potentially relevant documents
- c. By replacing the BERT model with a linear classifier
- d. NONE of the other options is correct
- e. By training the BERT model on a sentiment analysis dataset rather than a relevance dataset

### **Q15.** In the context of information retrieval, what are the required steps in the training stage of the two-stage (re)ranking process?
- a. Top k retrieval, Feature extraction, Labeling, Learning
- b. None of the above
- c. Corpus indexing, Stopword removal, Stemming, Training Embeddings
- d. Query expansion, Dimensionality reduction, Clustering, Re-ranking
- e. Document filtering, Term weighting, Relevance scoring, Feedback loop

### **Q16.** Which of the following is (are) NOT a common ranking function(s) used in term-based information retrieval?
- a. BM25
- b. TF-IDF
- c. Vector Space Model with Cosine Similarity
- d. Jaccard Coefficient
- e. NDCG
- f. PageRank
- g. Levenshtein Distance
- h. NONE of the other options are correct
- i. Binary cross-entropy
- j. ROUGE-L


### **Q17.** In an information retrieval context, what is a "posting list"?
- a. a list of documents that match a specific keyword query
- b. a list of all words present in a specific document
- c. a list of document identifiers containing a given term, along with frequency metrics
- d. a list of the most frequent queries entered by users
- e. NONE of the other answers is correct

### **Q18.** In term-weighting schemes like TF-IDF, the "IDF" term is included to:
- a. boost the weight of frequent terms within a specific document
- b. reduce the weight of terms that occur frequently across the entire corpus
- c. normalise the length of the document vector
- d. handle out-of-vocabulary terms during testing
- e. NONE of the other answers is correct

### **Q19.** What is the main advantage of an "inverted index" in a text search system?
- a. it reduces the storage requirement of the corpus by half
- b. it allows for sub-linear time retrieval of documents containing query terms
- c. it automatically corrects spelling mistakes in the user query
- d. it ranks documents based on user popularity rather than lexical match
- e. NONE of the other answers is correct

### **Q20.** In evaluating a text retrieval system, "Mean Average Precision" (MAP) measures:
- a. the percentage of relevant documents retrieved in the top 1 result
- b. the average precision across multiple queries, taking into account the rank of each relevant document
- c. the ratio of true positives to false positives across the corpus
- d. the lexical similarity between the query and the top-ranked document
- e. NONE of the other answers is correct

---

## Language modelling & Word Embeddings

### **Q137.** Which of the following techniques might be used to discover the topics discussed in a collection of documents?
- a. TF-IDF cosine similarity
- b. Word2Vec embedding
- c. Latent Dirichlet Allocation (LDA)
- d. NONE of the other answers is correct
- e. Tokenisation algorithm
- f. Support Vector Machine classifier

### **Q138.** Latent Dirichlet Allocation (LDA) can be used to:
- a. classify documents into a predefined set of categories
- b. cluster words based on their structural properties
- c. automatically parse the syntactical structure of a sentence
- d. discover the hidden topics discussed in a collection of documents
- e. NONE of the other options is correct
  
### **Q12.** A statistical language model computes:
- a. NONE of the other options are correct
- b. a probability distribution over different languages for a piece of text
- c. a probability distribution over emotions (happiness, sadness, anger, etc.) for a piece of text
- d. a probability distribution over sequences of words in a piece of text
- e. a parse tree for statistical programming languages like R, SAS, etc.
- f. a graph structure of the relationships linking the Named Entities present in the text
- g. the acoustic signal in a text-to-speech system
- h. statistics like the average document length, the average vocabulary size and the average token length in a collection of documents
- i. a probability distribution over grammatical classes (verbs, nouns, etc.) appearing in some text

### **Q13.** Given the following conditional probabilities for a trigram language model:
P("I") = 1/4, P("like") = 1/10, P("chocolate") = 1/10, P("ice") = 1/10, P("cream") = 1/8 ...  
P("ice" | "I") = 1/20, P("like" | "I") = 1/2 ...  
P("chocolate" | "I","like") = 1/4, P("ice" | "like","chocolate") = 1/2, P("cream" | "chocolate","ice") = 1/2 ...  
What is the probability of the sequence "I like chocolate ice cream"?
- a. 1/128
- b. 1/10
- c. 1/6400
- d. 1/160
- e. Insufficient information provided in the question to calculate an answer
- f. NONE of the other answers are correct
- g. 1/32
- h. 1/256
- i. 1/640
- j. 1/64
- k. 1/32000
- l. 1/320

### **Q15.** If the probability of the sequence "we really like NLP" was exactly 1/16, what would the perplexity of the sentence be? (Assume the sentence is tokenised at the word level.)
- a. 2
- b. 16
- c. 0
- d. 1/2
- e. 1/16
- f. 8
- g. NONE of the other answers is correct
- h. 4
- i. 64
- j. 1
- k. 1/4

### **Q16.** Should we prefer language models with higher perplexity or lower perplexity?
- a. higher perplexity
- b. depends on the context (e.g. whether task is question answering or translation)
- c. lower perplexity
- d. perplexity is used to evaluate clustering algorithms, not language models
- e. NONE of the other answers is correct
- f. perplexity is used to train the model and thus cannot be used to evaluate it

### **Q17.** Consider a bigram language model with the following marginal and conditional probabilities:
P(a)=1/2, P(b)=1/4, P(c)=1/8, P(d)=1/8  
P(b|a)=1/2, P(c|a)=1/2, P(a|b)=1/8, P(b|b)=1/4, P(c|b)=1/8, P(d|b)=1/4  
P(a|c)=1/3, P(b|c)=1/6, P(c|c)=1/6, P(d|c)=1/3, P(b|d)=1 (all others = 0)  
Using top-k sampling with k set to 2, what is the probability of seeing the output "a b c"?
- a. 1/16
- b. 1/32
- c. 1/128
- d. 1/64
- e. 1/2
- f. 1/6
- g. 1/8
- h. 1/3
- i. 1/4
- j. 1/12
- k. 1
- l. NONE of the other options are correct
- m. 0

### **Q151.** Consider a bigram language model with the following marginal and conditional probabilities:
P(a)=1/2, P(b)=1/4, P(c)=1/8, P(d)=1/8  
P(b|a)=1/2, P(c|a)=1/2, P(a|b)=1/8, P(b|b)=1/4, P(c|b)=1/8, P(d|b)=1/4  
P(a|c)=1/3, P(b|c)=1/6, P(c|c)=1/6, P(d|c)=1/3, P(b|d)=1 (all others = 0)  
What is the probability of seeing the output "a b d b"?
- a. 1/16
- b. 1/32
- c. 1/128
- d. 1/64
- e. 1/2
- f. 1/6
- g. 1/8
- h. 1/3
- i. 1/4
- j. 1/12
- k. 1
- l. NONE of the other options are correct

### **Q152.** Given a vocabulary size V and an ngram order n, what is the maximum number of unique counts that a language model might need to store?
- a. V + n
- b. n^V
- c. V^n
- d. V * n
- e. NONE of the other options are correct

### **Q153.** If a model is trained on a tiny corpus of text, what effect is this likely to have on its perplexity when evaluated on a large, independent test set?
- a. perplexity will be extremely high (or infinite)
- b. perplexity will be extremely low (close to zero)
- c. perplexity is unaffected by the size of the training corpus
- d. perplexity cannot be calculated under these conditions
- e. NONE of the other choices is correct
  
### **Q18.** Which statement about the limitations of Ngram language models is NOT correct?
- a. the training corpus is never big enough to estimate high-order ngrams well
- b. storing counts for high-order ngrams requires massive amounts of memory
- c. predictive performance of an ngram model depends greatly on the maximum ngram length (order of the model)
- d. NONE of the other answers is correct
- e. the expected number of occurrences of an n-gram decreases linearly with the length of the ngram

### **Q19.** When Markov language models are used to estimate the probability of the next word in a sentence, which of the following is NOT one of the techniques applied to improve quality of probability estimates?
- a. interpolating higher and lower estimates
- b. removing extremely high frequency n-grams, including stop-words
- c. smoothing probability estimates by adding a small constant to all word counts
- d. none of the other options are correct
- e. backing-off the estimator to use estimates from lower-order n-grams if counts for higher order ones are zero


### **Q21.** Assume that you have learnt GloVE embeddings of size 256 over a vocabulary of one million tokens. Approximately how much memory (in GB) is needed to store all of the embedding vectors using single precision (32-bit) floating point?
- a. 32GB
- b. 0.1MB
- c. None of the answers are correct
- d. 0.001GB
- e. 256GB
- f. 2GB
- g. 1GB
- h. 4GB

### **Q22.** Assume that you have learnt Word2Vec embeddings of size 512 over a vocabulary of four hundred thousand tokens. Approximately how much memory (in GB) is needed to store all of the vectors using double precision (64-bit) floating point?
- a. 2GB
- b. 8GB
- c. 6.4GB
- d. None of the answers are correct
- e. 3.2GB
- f. 1.6GB
- g. 0.4GB
- h. 12.8GB
- i. 0.8GB
- j. 4GB

### **Q23.** Which of the following sentences best describes the way we learn Word2Vec embeddings using the Skip-gram technique?
- a. NONE of the other answers is correct
- b. Within each context window, train the model to predict all surrounding words based on the single word at centre of context (i.e. use a one-hot vector to predict a bag-of-words vector)
- c. Within each context window, train the model to predict the central word based on all other words in the surrounding context (i.e. use a bag-of-words vector to predict a one-hot vector)
- d. Within each context window, train the model to predict the central word based on a single word in the surrounding context (i.e. use a one-hot vector to predict a one-hot vector)
- e. For each context window, train the model to predict the second half of the words in the context based on the first half of the words in the context

### **Q24.** Which statement about Word2Vec is true?
- a. Word2Vec is based on a recurrent neural network architecture
- b. Word2Vec is trained to predict whether a missing word fits given a particular surrounding context
- c. Word2Vec learns sparse vector representations for words
- d. NONE of the other statements is true
- e. Word2Vec learns dense vector representations for documents

### **Q25.** Which method is often used to represent words as numerical vectors in NLP?
- a. Recurrent Neural Networks
- b. Word2Vec
- c. Topic modeling
- d. TF-IDF
- e. NONE of the other methods can be used
- f. Naive Bayes

### **Q26.** GloVE embeddings:
- a. represent images as numerical vectors
- b. provide a low dimensional approximation of a high dimensional representation
- c. provide a sparse representation
- d. represent words as numerical vectors
- e. represent topics as numerical vectors
- f. NONE of the other answers are correct
- g. represent documents as numerical vectors

### **Q27.** Which statement about the uses of word embeddings is NOT generally true?
- a. word embeddings directly solve the problem of negation, and particularly nested negation, in sentiment analysis
- b. ALL of the other statements are generally true
- c. word embeddings have been used to mine scientific literature to help create new scientific hypotheses
- d. pre-trained word embeddings are available for many corpora and can be downloaded and applied to a new problem
- e. word embeddings tend to improve the performance of simple ML models on any NLP task

### **Q28.** Which of the following statements about the uses of word embeddings is generally true?
- a. pre-trained word embeddings are available for many corpora and can be downloaded and applied to a new problem
- b. ALL of the other statements are generally true
- c. word embeddings are useful for dealing with problems of synonymy (words with similar meanings) when searching for content
- d. word embeddings have been used to mine scientific literature to help create new scientific hypotheses
- e. word embeddings tend to improve the performance on any NLP task

### **Q29.** Which of the following is NOT usually a property of word embeddings?
- a. the euclidean length of the embedding vector encodes the importance prior (unigram) probability of the word
- b. semantically related concepts tend to occur close to each other in the embedding space
- c. linear translations in the embedding space can encode morphological transformations (e.g. convert present tense to past tense)
- d. ALL of the other answers are valid properties of most word embeddings
- e. all of the possible meanings are encoded in the word vector
- f. semantic relationships (such as "capitol-city of") can be extracted by averaging the difference between the source and target word vectors

### **Q30.** Which of the following is NOT a property of Word2Vec word embeddings?
- a. the sum of the embeddings of the characters present in a word is equal to the embedding of the word itself
- b. linear translations in the embedding space can encode morphological transformations
- c. semantically related concepts tend to occur close to each other in the embedding space
- d. ALL of the other answers are valid
- e. semantic relationships (such as "capitol-city of") can be extracted by averaging the difference between source and target word vectors
- f. for words with multiple possible meanings all of the possible meanings are encoded in the word vector

### **Q31.** Which of the following statements about sub-word embeddings is NOT usually true?
- a. FastText is an example of subword embedding
- b. sub-word embeddings solve the problem of not being able to represent unseen (out-of-vocabulary) words at test time
- c. sub-word embeddings are sub-optimal with respect to full-word embeddings because they lose too much information
- d. ALL of the other answers are correct
- e. Tokenizers that employ byte-pair-encoding cause the resulting network to learn a sub-word embedding
- f. sub-word embeddings split words up into smaller units and learn an embedding vector for each

### **Q121.** What effect does Byte-Pair Encoding (BPE) achieve in Transformer models?
- a. ALL of the other answers are CORRECT
- b. improves performance of the Transformer by taking advantage of morphology of the language
- c. reduces the vocabulary size with respect to a word-level tokeniser
- d. allows common suffixes to be removed from words and treated separately
- e. increases vocabulary size with respect to a character-level tokenizer
- f. reduces the sequence length by grouping frequent character sequences together

### **Q122.** Byte-pair encoding:
- a. is a way of quantising the parameters of a transformer such that they only occupy 2 bytes each (half-precision representation)
- b. agglomerates common consecutive characters together to form sub-word tokens
- c. represents each word as a byte-pair vector, which is similar to a one-hot vector but with two non-zero values in it
- d. none of the other options is correct
- e. encodes text as byte-pairs: 2 bytes for each character in the text

### **Q123.** What are ASCII and UTF-8, and what is the difference between them?
- a. None of the other options are correct
- b. Multimedia file formats: main difference is that ASCII is a plain text format, while UTF-8 is a binary format allowing for richer media content
- c. Encryption algorithms: main difference is that ASCII uses symmetric encryption, while UTF-8 uses asymmetric encryption
- d. Web development languages: main difference is that ASCII is primarily used for client-side scripting, while UTF-8 is used for server-side scripting
- e. Character encoding standards: main difference is that ASCII supports only basic English characters, while UTF-8 can represent characters from many languages

### **Q124.** Which of the following is a character encoding standard that can represent characters from many different languages?
- a. Byte-pair encoding
- b. FastText
- c. UTF-8
- d. ASCII
- e. NONE of the other options are correct
  
### **Q32.** The English word "hippopotomonstrosesquipedaliophobia" refers to the "fear of monstrously long words". Which of the following well-known technologies could deal well with a text containing this monstrously long word?
- a. NONE of the other well-known technologies would deal well with this word
- b. hippopotoBERT
- c. HNSW
- d. Lemmatisation
- e. Word2Vec
- f. FastText
- g. SVMs

### **Q33.** Given the piece of text "This exam is too much" and a trigram language model, what is the chance that the model produces the word "fun" as the next token if top-k sampling is used with k set to 5? *(Top 5: work 3%, effort 2.5%, fun 2%, food 1.5%, time 1%)*
- a. 20%
- b. 0%
- c. 50%
- d. 2.5%
- e. 2%
- f. 22%
- g. 10%
- h. NONE of the other answers be correct
- i. 4%
- j. Insufficient information provided in the question to calculate an answer


### **Q35.** Which statement about Deep Neural Networks (DNNs) used in NLP is NOT true?
- a. DNNs are inherently linear models and thus cannot learn complex non-linear combinations of features
- b. DNNs typically require a large amount of text data to train effectively from scratch
- c. pre-training on a large corpus followed by fine-tuning on a specific task is a common strategy
- d. ALL of the other options are true
- e. DNNs learn a hierarchy of useful features automatically from raw data
- f. DNNs can be more difficult to train than simpler models
- g. DNNs require large computing resources (GPUs)

### **Q36.** If the probability of the sequence "Vincenzo was the best tutor I ever had" was exactly 1/256, what would the perplexity of the sentence be? (Assume tokenisation at the word level.)
- a. 4
- b. 1
- c. 1/256
- d. 0
- e. NONE of the other answers is correct
- f. 2
- g. 256
- h. 1/2
- i. 8
- j. 16
- k. 1/16

### **Q165.** Which embedding technique is explicitly built upon a global term-co-occurrence matrix factorisation approach?
- a. Word2Vec Continuous Bag of Words (CBOW)
- b. Word2Vec Skip-gram
- c. GloVe
- d. FastText
- e. One-hot encoding

### **Q166.** What does the "cosine similarity" between two word vectors measure?
- a. the Euclidean distance between their endpoints
- b. the angle between the vectors, reflecting structural semantic similarity independent of magnitude
- c. the sum of the magnitudes of the two vectors
- d. the difference in frequency between the two words in the corpus
- e. NONE of the other options are correct

### **Q167.** Why can standard full-word embeddings like Word2Vec NOT represent the word "unbelievability" if it never appeared in the training set?
- a. Because the word is too long to fit into the memory cache
- b. Because full-word embedding architectures assign a unique index to each vocabulary word, leading to out-of-vocabulary limitations for unseen strings
- c. Because the word contains negative morphological prefixes
- d. Because cosine similarity fails on multi-syllabic tokens
- e. NONE of the other answers is correct

### **Q168.** The property of vector arithmetic in word embeddings where `vec("King") - vec("Man") + vec("Woman") ≈ vec("Queen")` demonstrates:
- a. that word embeddings are completely random
- b. that the embedding space encodes semantic and analogical linear relationships
- c. that neural networks are unable to handle grammar rules
- d. that document length affects token similarity
- e. NONE of the other options are correct

### **Q169.** What optimization trick does Word2Vec Skip-gram use to avoid calculating the full softmax denominator over a massive vocabulary?
- a. Dropout
- b. Batch Normalisation
- c. Negative Sampling
- d. Layer Normalisation
- e. Greedy Search

---

## Text Pre-processing

### **Q117.** Which of the following is **NOT** a text pre-processing step in an NLP application?
- a. ALL of the other options are common preprocessing activities
- b. Masked language modeling
- c. Removing HTML markup
- d. Removing stopwords
- e. Removing low-frequency terms
- f. Case-folding
- g. Tokenization
- h. Spelling correction
- i. Lemmatization/Stemming

### **Q118.** Which of the following is a **common** text pre-processing step in an NLP application?
- a. Tokenization
- b. Removing HTML markup
- c. ALL of the other options are common preprocessing activities
- d. Lemmatization or stemming
- e. Stopword removal
- f. Case-folding

### **Q119.** Word normalisation is the process of:
- a. NONE of the other options are correct
- b. padding the input sequence to BERT so that each sequence has exactly the same length
- c. dividing the word embedding vector by its L2 norm, so that it has a Euclidean length of 1
- d. removing profanities (swear words) and other inappropriate content from a piece of text
- e. aligning words to a common reference dictionary (e.g. by removing punctuation), so as to ensure consistent spelling/formatting throughout the corpus

### **Q120.** What is the difference between stemming and lemmatization?
- a. Stemming is a simple algorithm that applies rules to remove suffixes from word stems, while lemmatization is a more sophisticated technique that uses a dictionary and morphological analysis to extract the lemma
- b. Lemmatization is a simple algorithm that applies rules to remove suffixes from word lemmas, while stemming is a more sophisticated technique that uses a dictionary and morphological analysis to extract the stem
- c. Stemming and lemmatization are exactly the same
- d. Stemming involves finding the STEM (Science Technology Engineering and Mathematics) terms in the text, while lemmatisation searches only for the lemmas (mathematical equations) in the text
- e. NONE of the other options are correct
- f. Stemming involves finding the stem word in the sentence (i.e. the subject of the sentence), while lemmatisation searches for the lemma, which is the primary verb in the sentence

### **Q130.** Which of the following statements about the most frequently occurring words in a corpus is true?
- a. they are the most important words in the query
- b. they result in short posting lists
- c. they should never be removed during preprocessing
- d. they are the most discriminative words in any document
- e. NONE of the other answers are correct

### **Q131.** In Information Theory, the logarithm of one over the probability of an event corresponds to:
- a. the optimal parameter setting for that feature
- b. the chance that the event will happen again
- c. the amount of information learnt from the event
- d. the number of times the event occurs
- e. nothing — in information theory, the exponent of the probability is important, not its logarithm
- f. NONE of the other options is correct
  
---

## RNN

### **Q161.** What type of neural network layer is primarily used to process grid-like structures such as images, but has also been adapted for local feature extraction in NLP text arrays?
- a. Recurrent Layer
- b. Linear Layer
- c. Convolutional Layer
- d. Attention Layer
- e. Embedding Layer

### **Q163.** Which activation function is defined by the formula `f(x) = max(0, x)`?
- a. Sigmoid
- b. Tanh
- c. ReLU
- d. Softmax
- e. GeLU

### **Q164.** What problem can occur when training very deep networks where gradients become progressively smaller as they are backpropagated to earlier layers?
- a. Overfitting
- b. Exploding Gradients
- c. Vanishing Gradients
- d. Underfitting
- e. Symmetry Breaking


### **Q40.** What makes training RNNs particularly slow?
- a. very small values of the learning rate must be used to prevent instability of the training procedure
- b. the need to propagate gradient information sequentially back through the entire text sequence
- c. hardware limitations often lead to memory bottlenecks where the GPU becomes underutilised waiting for data to load from main memory
- d. optimisation techniques were designed to optimise CNNs rather than RNNs which are sequential
- e. the loss function becomes particularly complicated for an RNN, with lots of sequential terms
- f. they require an immense amount of data to train properly
- g. NONE of the other options is correct

### **Q41.** Which statement about a Long Short-Term Memory (LSTM) network is NOT true?
- a. an LSTM is a type of recurrent neural network that by default passes state information directly from input to output
- b. due to its architecture it is not possible to stack LSTMs on top of each other
- c. ALL other options are correct
- d. an LSTM is a network with an ability to forget information
- e. an LSTM is a network that can learn what information to remember and when to do so

### **Q42.** Which of the following statements about Recurrent Neural Networks (RNN) is NOT true?
- a. ALL of the other options are correct
- b. an RNN can be used to process arbitrarily long input sequences
- c. an RNN is no more expensive to learn than an SVM for the same task
- d. an RNN is able to generate text representations that account for word order, such that "white snow" and "snow white" are not the same
- e. an RNN is a function that takes two input vectors and returns two output vectors
- f. an RNN can deal well with nested negation in a sentence like "It is not that I don't think that he didn't write an amazing exam."

### **Q43.** Whenever data scientists work with sequential data (such as HTML code, programming code, binary executables, protein sequences, or audio speech signals):
- a. techniques from NLP are often applicable
- b. one must apply Sequence Labelling techniques
- c. NONE of the other answers are correct
- d. techniques from NLP are rarely applicable

---

## ReGex

### **Q38.** The fact that the exclamation mark '!' can denote a factorial (4! = 1\*2\*3\*4), the question mark '?' can indicate a missing value (2, 4, ?, 16, 32), and the period '.' can be a decimal point (4.56), complicates which NLP task?
- a. POS tagging
- b. NONE of the other answers are correct
- c. Classification
- d. Clustering
- e. Sentence segmentation
- f. Named Entity Extraction

### **Q39.** When processing textual documents, which of the following techniques is commonly used for defining patterns and extracting information from the text?
- a. Hidden Markov Models
- b. Decision trees
- c. K-means clustering
- d. Support Vector Machines
- e. Regular expressions
- f. NONE of the other options are correct

### **Q147.** Which one of the following regular expressions would match a student email of the form "first.lastname@mail.polimi.it"?
- a. `[a-zA-Z0-9]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}`
- b. `[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+.[a-zA-Z]{4,}`
- c. NONE of the other regular expressions would match the desired email address
- d. ALL of the other regular expressions would match the desired email address
- e. `[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}`
- f. `[a-zA-Z0-9._-]+@[0-9.-]+\.[a-zA-Z]+`
- g. `[a-zA-Z0-9]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}`

### **Q148.** Which, if any, of the following strings would the regular expression `[A-Z]{6}\d{2}[A-Z]\d{2}[A-Z]\d{3}[A-Z]` match?
- a. ABCDEF8213H521JJ
- b. ABCDE82G13H521JJ
- c. ABCDEF8G13H521JJ
- d. ABCDEF82G13H521J
- e. ALL of these strings would match the regular expression
- f. NONE of these strings would match the regular expression
- g. ABCDEFG8213H521JJ

### **Q149.** Which one of the following options is NOT a valid Regular Expression component?
- a. `\d` matches any decimal digit
- b. `*` matches zero or more occurrences of the preceding expression
- c. `+` matches one or more occurrences of the preceding expression
- d. `?` matches zero or one occurrence of the preceding expression
- e. `\w` matches any whitespace character
- f. `.` matches any single character except newline
- g. ALL of the options are valid components

### **Q150.** Regular expressions are widely used in NLP applications for:
- a. training word embedding models
- b. tokenising, normalising and text pattern matching rules
- c. learning deep neural network architectures
- d. computing cosine similarity scores between text document representations
- e. NONE of the other options is correct

### **Q125.** Consider the following regular expression:
`regex = "(\\:\\w+\\:|\\<[\\/\\]?3|[\ \\\\D|\\*\\$][\\-\\^]?[\\:\\;\\=]|[\\:\\;\\=B8][\\-\\^]?[3DOPp\\@\\$\\*\\\\)\\(\\/\\|])(?=\\s|[\\!\\.\\?]|$)"`
Which one of the following types of content matches the regular expression?
- a. NONE of the other options is correct
- b. punctuation (e.g. ';', ':', '?'...)
- c. only symbols like '@', '#', '*', ...
- d. ALL other options are correct
- e. emojis
- f. numbers

### **Q126.** Consider the regular expression: `\d{1,2}-(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)-\d{2,4}`
Which, if any, of the following strings would the expression match?
- a. 21 May 2025
- b. 2023-Apr-25
- c. 1:Jan:0000
- d. 3-Mar-123
- e. NONE of these strings would match the regular expression
- f. ALL of these strings would match the regular expression
- g. 29-Fe-2000
- h. 01--Jun--2012

### **Q127.** Regular expressions provide a powerful language for writing rules to extract content from text documents, but have various limitations. Which of the following would NOT be considered a limitation of regular-expression based text extraction?
- a. false positives, due to insufficiency of syntactical structure to prevent them
- b. the difficulty of writing extraction rules by hand
- c. the difficulty/inability to integrate knowledge of context around the extracted entity
- d. false negatives, due to lack of generality of the rule used
- e. the simplicity of the approach
- f. NONE of the other options are correct
  
---

## Sequence-to-Sequence Models & Transformers

### **Q44.** How does a self-attention mechanism update embedding vectors?
- a. NONE of the other answers is correct
- b. through the use of recurrent connections between embeddings at subsequent token positions
- c. by multiplying the input vector by a set of fixed attention weights
- d. by calculating the similarity between embeddings in different positions and using that similarity to weight the vectors
- e. by using pre-trained embeddings
- f. by making use of the random initialisation

### **Q45.** Consider a self-attention block of a transformer decoder model. Assume that when we input vectors representing the sentence "I like cats and", the model generates the vector for the word "dogs". If we changed the sentence to be "I dislike cats and", which parts of the self-attention formula `softmax(Q·Kᵀ / √dk) · V` would be affected?
- a. K
- b. Nothing changes
- c. V and Q
- d. Q and K and V
- e. Q
- f. Q and K
- g. K and V
- h. V

### **Q46.** The diagram shows an implementation of an attention mechanism. What names are usually given to A, B, and C?

<img width="229" height="215" alt="image" src="https://github.com/user-attachments/assets/06460559-1309-4c7a-8958-d67d3c4cbb4f" />

- a. NONE of the other options is correct
- b. A: value, B: attention, C: query
- c. A: query, B: lock, C: key
- d. A: value, B: lock, C: key
- e. A: query, B: key, C: value
- f. A: value, B: key, C: query
- g. A: lock, B: key, C: value
- h. A: query, B: key, C: value
- i. A: value, B: query, C: key
- j. A: key, B: value, C: query

### **Q47.** The formula shown is sometimes used to compute similarity within the attention mechanism of a sequence-to-sequence model. Which (if any) of the following statements about the formula is NOT correct?
$$\text{similarity}(\vec{h}_{i-1}, \vec{e}_j) = \frac{\vec{h}_{i-1} \cdot \vec{e}_j}{\sqrt{d}}$$

- a. The variable "d" denotes the number of dimensions of the embedding vector
- b. The variable "h" denotes the previous state of the decoder
- c. The formula computes multiplicative (rather than additive) attention weights
- d. ALL of the other statements are CORRECT
- e. The denominator normalizes the dot product to have a standard deviation of 1
- f. The variable "e" denotes an embedding vector for a certain position produced by the encoder

### **Q48.** Which statement about positional embeddings used in Transformer architectures is NOT true?
- a. recent models employ ROPE which rotates token embeddings to encode their relative position
- b. absolute positional encodings make generalising to longer contexts difficult
- c. the original Transformer used additive sinusoidal position embeddings
- d. some Transformer architectures have made use of learnt positional embeddings
- e. some Transformer models use relative position embeddings where a learnt bias is included in the similarity calculation
- f. ALL of the other statements are correct
- g. rotary position embeddings have speed advantages over relative position embeddings
- h. relative position embeddings allows for longer contexts, but slows the self-attention calculation

### **Q49.** Suppose we define a new positional encoding scheme where the embedding for position k is the binary encoding of k. Based on the cosine similarity plot, what are the most obvious issues with this approach?
- a. Binary codes require more storage than float encodings
- b. Adjacent positions may be less similar than further apart ones
- c. All positions eventually converge to the same encoding
- d. All of the above
- e. The encoding dimension must grow exponentially with sequence length

### **Q50.** What technique is used to break the symmetry with respect to the input token positions within a Transformer model?
- a. no technique is used to break the symmetry, since it is a useful property of the model
- b. use of asymmetric encoder and decoder structures
- c. the self-attention mechanism
- d. addition of recurrent connections between positions
- e. convolutions over the input embeddings
- f. byte-pair encodings
- g. NONE of the other answers are correct
- h. positional embeddings or rotations

### **Q51.** What mechanism allows a model to focus on specific parts of the input text when making predictions?
- a. Attention
- b. Pooling
- c. Regularisation
- d. Convolution
- e. Dropout
- f. Fine-tuning
- g. NONE of the other answers is correct

### **Q52.** Which NLP task is being performed (implicitly) by the self-attention mechanism when it resolves pronoun references in sentences like "The animal didn't cross the street because it was too tired"?
- a. The self-attention mechanism is not implicitly performing any of the other tasks
- b. Sentiment Analysis
- c. Information Extraction
- d. Named Entity Recognition
- e. Text Retrieval
- f. Coreference Resolution
- g. Acronym Expansion
- h. Part-of-Speech Tagging
- i. Delexicalisation

### **Q53.** In order to speed up model training, the Transformer model REMOVED what part of the sequence-to-sequence with attention model architecture?
- a. the attention mechanism connecting the encoder to the decoder
- b. the normalization layer
- c. the encoder network
- d. the decoder network
- e. the feedforward network
- f. the recurrent links within the encoder and decoder
- g. NONE of the other options is correct
- h. the self-attention layer

### **Q54.** Which technique used in NLP is the most recent and considered state-of-the-art?
- a. Conditional Random Fields
- b. Recurrent Neural Networks
- c. Hidden Markov models
- d. Transformer models
- e. Ngram Language Models
- f. Topic Models
- g. Finite state automata
- h. Support Vector Machines
- i. Context-free grammars

### **Q55.** Which statement about the BERT model is NOT true?
- a. BERT is a bidirectional model
- b. ALL of the other answers are correct
- c. BERT models have hundreds of millions parameters (or more)
- d. BERT models make for excellent text classifiers
- e. BERT works directly on text sequence, so when fine-tuning a text classifier, there is no need to first extract BOW feature representation
- f. multilingual BERT can be fine-tuned on examples in one natural language and applied on another
- g. BERT models are pre-trained on masked language modelling task

### **Q56.** Which Machine Learning model makes use of a bidirectional Transformer architecture to extract a feature representation of text?
- a. GPT-2
- b. Wav2Vec
- c. K-means
- d. BERT
- e. Naive Bayes
- f. NONE of the other answers is correct
- g. Word2Vec
- h. SVM
- i. XGBoost

### **Q57.** You train a multilingual BERT based classifier and find that the model is performing particularly poorly. What might you do to improve performance?
- a. check whether a monolingual BERT model exists for your language and if so, test it
- b. ALL of the other answers are valid
- c. train it for another epoch to see if the validation performance increases
- d. try increasing the batch size if memory on the GPU allows
- e. try to train a larger version of the BERT model
- f. re-start the training with a lower setting of the learning rate

### **Q58.** What special tokens are often used to fine-tune a BERT model for pairwise text classification tasks?
- a. NONE of the other options is correct
- b. [BEGIN], [INSIDE] and [OUTSIDE]
- c. [INIT], [MIDDLE] and [TERM]
- d. [CLS] and [SEP]
- e. [START] and [END]
- f. [OPEN] and [CLOSE]

### **Q59.** Which statement about GPT (GPT-2, GPT-3, etc) models is NOT true?
- a. GPT stands for Generative Pre-trained Transformer
- b. GPT is a bidirectional text encoder
- c. ChatGPT is based on a recent version of the GPT model
- d. ALL of the other answers are correct
- e. GPT models are preferred over BERT models for text generation tasks

### **Q60.** Which statement about the T5 (Text-To-Text Transfer Transformer) model is NOT true?
- a. T5 makes use of bidirectional encoder and causal decoder
- b. T5 makes use of a relative positional encoding
- c. T5 is particularly useful for translation tasks
- d. ALL of the other answers are correct
- e. T5 is a distilled (smaller) version of BERT
- f. T5 can generate a response and thus can be trained for dialog tasks
- g. T5 has an encoder-decoder architecture just like in the original transformer paper ("Attention is all you need")

### **Q61.** How was it possible for a GPT-2 model to learn how to translate text from English to French if it was trained on a corpus of English (but not French) documents?
- a. It inherently understands multiple languages without needing to train on them
- b. It is based on an Encoder-Decoder Transformer architecture that was designed for translation tasks
- c. It applies statistical machine translation techniques
- d. NONE of the other answers are correct
- e. It used external translation APIs
- f. It learnt from examples of translation patterns that were embedded within the English documents

### **Q62.** We loaded a pretrained BERT model from HuggingFace (BertForSequenceClassification) with `Embedding(105879, 768)`, `position_embeddings: Embedding(512, 768)`, 12 BertLayers, and `classifier: Linear(768, 4)`. Which of the following statements is False?
- a. The vocabulary size is 105879
- b. The model uses 768 hidden dimensions
- c. The model can process text segments up to 512 tokens long
- d. The model is configured to classify text into 4 categories
- e. NONE of the statements are False

### **Q65.** Which of the following tasks could NOT be modelled as a sequence-to-sequence problem?
- a. ALL of the other tasks could be treated as sequence-to-sequence problems
- b. Summarisation (e.g. summarise a patient medical health history for a doctor to read)
- c. Question answering (e.g. answer doctor's questions about patient based on text in patient's file)
- d. Translation (e.g. translate official document containing medical jargon into plain language)
- e. Anonymisation (e.g. remove sensitive information from a hospital discharge letter)

### **Q170.** In a Transformer model, why do we multiply the queries and keys matrix by `1 / sqrt(d_k)` inside the softmax?
- a. to reduce the number of parameters in the model
- b. to prevent the dot-products from growing too large in magnitude, which would push the softmax function into regions with dangerously small gradients
- c. to break the position symmetry of input tokens
- d. to enforce causal masking during generation
- e. NONE of the other answers is correct

### **Q171.** What type of attention mechanism is used in the decoder of a Transformer model to ensure it cannot look at future tokens?
- a. Multi-head Attention
- b. Cross Attention
- c. Masked / Causal Self-Attention
- d. Bidirectional Attention
- e. Sparse Attention

### **Q172.** "Multi-head attention" allows the model to:
- a. compress the prompt length dynamically
- b. attend to information from different representation subspaces at different positions simultaneously
- c. run on multiple GPUs without communicating parameters
- d. substitute the feed-forward network block entirely
- e. NONE of the other options is correct

### **Q173.** In a Transformer block, what is the role of the "Residual Connection"?
- a. to store hidden tokens for later retrieval tasks
- b. to pass position details directly to the output layer
- c. to allow gradients to flow directly through blocks without passing solely through non-linear layers, mitigating vanishing gradient issues
- d. to enforce strict sorting parameters on sequence indices
- e. NONE of the other options are correct

### **Q174.** What is the purpose of the "Layer Normalisation" step in a Transformer layer?
- a. it scales the vocabulary size to a power of 2
- b. it normalises activations across features within a single training example to stabilize training dynamics
- c. it flattens the matrix into a single-dimensional array
- d. it eliminates the need for activation functions like ReLU or GeLU
- e. NONE of the other options are correct

### **Q175.** Which architecture typically discards the encoder stack entirely, relying instead on autoregressive blocks to predict the subsequent token?
- a. BERT
- b. RoBERTa
- c. Decoder-Only Models (e.g., GPT, Llama)
- d. T5
- e. DeBERTa
  
### **Q176.** What is a major disadvantage of using absolute positional encodings like sinusoidal vectors?
- a. They add too many trainable parameters to the base model
- b. They fail to generalise or extrapolate effectively to sequence lengths longer than those seen during model pre-training
- c. They make the attention matrix asymmetric by default
- d. They can only be used with word-level tokenisers
- e. NONE of the other choices is correct
  
---

## Applications of BERT and  GPT

### **Q66.** When generating text from a language model, which of the following techniques will likely require the most computational resources and thus be slowest to generate text?
- a. top-k sampling
- b. random sampling
- c. greedy sampling
- d. impossible to answer this question with the information provided
- e. beam search

### **Q67.** When generating text using a language model, which of the following is NOT a usual method to generate text?
- a. ALL of the other answers are valid methods
- b. Top-k sampling
- c. Temperature-controlled sampling
- d. Greedy search
- e. Random sampling
- f. Beam search
- g. Stratified sampling

### **Q68.** When generating text from a language model with top-k sampling, setting the value of k to the size of the vocabulary is equivalent to performing:
- a. beam search
- b. random sampling
- c. NONE of the other answers is correct
- d. greedy sampling
- e. t-SNE dimensionality reduction

### **Q177.** In text generation, "Beam Search" differs from "Greedy Search" by:
- a. choosing a random token at each generation step based on temperature distributions
- b. keeping track of a fixed number (beam width) of the most probable partial sequences at each step rather than just the single best token
- c. parsing the document from right to left instead of left to right
- d. removing duplicate n-grams dynamically via regular expression matches
- e. NONE of the other options is correct

### **Q155.** What is the purpose of "Good-Turing smoothing"?
- a. to reduce the memory footprint of an ngram language model
- b. to approximate high-order ngrams using low-rank factorisation
- c. to re-estimate the probability of unseen or low-frequency n-grams based on the frequency of other low-frequency n-grams
- d. to smooth out the audio signal in a speech recognition system
- e. NONE of the other answers is correct


### **Q178.** What does the "Temperature" parameter control during token sampling?
- a. the speed at which the GPU processes text blocks
- b. the scale of the logits before applying softmax, where higher values flatten the distribution and introduce more randomness/creativity
- c. the context window limitation profile of the model
- d. the learning rate decay schedule during instruction tuning
- e. NONE of the other options are correct

### **Q179.** Top-p sampling (also known as Nucleus sampling) selects from:
- a. a fixed number of top tokens regardless of cumulative value
- b. the smallest possible set of top tokens whose cumulative probability exceeds the threshold p
- c. tokens that have prime number indices in the tokenizer vocabulary matrix
- d. positions matching absolute sinusoidal indices exclusively
- e. NONE of the other answers is correct

### **Q180.** Why can text generated using pure Greedy Search sometimes become stuck in repetitive loops?
- a. because the model parameters change dynamically during inference
- b. because it deterministically selects the local maximum token, which can lead the context path into highly predictable, cyclic logit loops
- c. because greedy search forces the model to execute backward passes during text output steps
- d. because vocabulary indices are arranged alphabetically
- e. NONE of the other choices is correct

### **Q181.** What is the purpose of a "repetition penalty" parameter during language model decoding?
- a. it throws a runtime error if the model repeats a word within 10 tokens
- b. it artificially discounts the logits of tokens that have already appeared in the generated text sequence, discouraging redundancy
- c. it increases the training loss if validation subsets overlap
- d. it scales down context parameters across multi-head attention blocks
- e. NONE of the other options are correct

### **Q69.** Given a bigram language model, what is the chance that the model produces the word "exam" as the next token after "amazing" if top-k sampling is used with k set to 10? *(Top 10 probabilities: grace 4%, food 3%, location 2%, experience 2%, people 2%, place 2%, minds 2%, experiences 1%, places 1%, exam 1%)*
- a. 5%
- b. 6%
- c. 1%
- d. NONE of the other answers are correct
- e. 10%
- f. 4%

### **Q70.** The code below tokenizes a piece of text and then applies a pre-trained decoder-only transformer to compute output logits for the prompt:

```python
# Tokenize the input string
input_encoding = tokenizer(input_string, return_tensors='pt').to(device)

# Get output logits
outputs = model(**input_encoding)
```

If we complete the program with the two pieces of code below, which one would produce the most probable token? *(Note that the second piece of code makes use of a softmax function, while the first doesn't.)*

 Code 1
```python
arg_max_idx = torch.argmax(outputs.logits[:, -1])
tokenizer.decode(arg_max_idx)
```

 Code 2
```python
p_dist_next = torch.softmax(outputs.logits[:, -1], dim=1)
arg_max_idx = torch.argmax(p_dist_next)
tokenizer.decode(arg_max_idx)
```
- a. Code 1 produces the most probable token
- b. Neither Code 1 nor Code 2 produces the most probable token
- c. Both solutions produce the most probable token
- d. Code 2 produces the most probable token

### **Q71.** When sampling text from a language model, setting the temperature to zero is equivalent to performing:
- a. Beam Search
- b. Top-k Sampling
- c. Random Sampling
- d. Greedy Sampling
- e. Temperature Sampling

### **Q72.** Robustness of an LLM-based question answering system would likely be improved by:
- a. removing the last few layers of the transformer stack
- b. multiplying all parameters of the model by a fixed constant (such as 3.14)
- c. using top-k sampling and setting the k to 1
- d. setting the Temperature of the sampler to zero
- e. sampling multiple generated sequences and then choosing the most frequent answer
- f. NONE of the other answers are correct

### **Q73.** In Multi-task learning, we fine-tune a language model to perform many different tasks at the same time. The aim/benefit of doing this is to get the model to:
- a. ALL the other answers are correct
- b. become so good at general-purpose question answering that it can generalise even to new domains
- c. learn to do many tasks contemporaneously, so we don't need to deploy and maintain many task-specific models
- d. generalise knowledge across the different tasks and thus perform better on any particular task

### **Q74.** Which of the following prompts to a language model would be considered an example of one-shot learning?
- a. "1 + 1 = 3, 1 + 3 = 4, 1 + 4 = 5, 1 + 5 ="
- b. "english: awesome exam, italiano: esame fantastico, english: mark rules, italiano:"
- c. "How do you say 'awesome exam' in French?"
- d. "apple => fruit, broccoli => vegetable, eggplant =>"
- e. ALL of the other approaches are correct examples

### **Q75.** Imagine providing the following prompt to a large language model with several joke examples labelled funny/not funny, ending with "I asked my dog what's two minus two. He said nothing. =>". What type of learning is the model doing in this case?
- a. one-shot learning
- b. few-shot learning
- c. NONE of the other answers are correct
- d. example-free learning
- e. fine-tuning
- f. gratis learning
- g. zero-shot learning

### **Q76.** Zero, one and few-shot learning involves:
- a. performing zero, one or few passes (epochs) over the training data
- b. fine-tuning a model using zero, one or few training examples respectively
- c. training a model from scratch using zero, one or few hidden layers respectively
- d. NONE of the other options is correct
- e. providing zero, one or few examples within the context window of a pre-trained model at test time, without performing any gradient updates

### **Q77.** For multi-modal retrieval, which type of model can be used to first align the embedding spaces of text and images?
- a. NONE of the other options is correct
- b. ResNet
- c. CLIP
- d. GPT-2
- e. FAISS
- f. BERT

### **Q78.** CLIP is a model primarily used for:
- a. reducing the length of a text document by removing punctuation, stopwords and low-frequency terms
- b. normalising text by removing acronyms, and converting dates to a standard format (dd-mm-yy) - c. converting speech audio signals into a text transcription
- d. learning a joint embedding space where text snippets and image documents can be directly compared
- e. NONE of the other answers is correct

### **Q79.** How might a GPT model best be used without fine-tuning?
- a. NONE of the other options is correct
- b. By using the pre-trained word embeddings to build a document representation
- c. By manually adjusting weights
- d. By training it to perform supervised learning tasks
- e. By applying zero-shot, one-shot, or few-shot learning

### **Q132.** Which of the following prompts would be the best if you are building an information extraction system using a few-shot learning approach?
- a. A prompt that contains a detailed description of the entity schema, constraints, rules, structural constraints, error profiles, along with 5 high quality input/output examples of matching structural formats and descriptions
- b. NONE of these approaches are valid
- c. A prompt that provides an instruction followed by 100 positive examples and 100 negative examples
- d. A generic template with placeholders for input data and an empty block where the output should go
- e. A short description of the entity we wish to extract

### **Q133.** Which of the following prompts would be the best if you are building a tool-calling application where the agent has access to 3 math tools?
- a. A detailed schema description of all tools including constraints and signatures, with instructions on returning format structural outputs, and clear guidelines on picking tools with multiple input/output pairs demonstrating step-by-step reasoning
- b. A generic instruction template with empty `{Instruction}`, `{Input}` placeholders
- c. A prompt with tools missing constraints but containing 10 examples of math questions
- d. NONE of these prompts are appropriate for tool-calling
- e. A prompt that tells the model it is a math professor and can solve any problem without explicitly mentioning tool signatures

### **Q134.** Which of the following prompts would be the best if you are building an agentic application that implements a reflex design pattern?
- a. A prompt that breaks down execution into execution loops, instructing the model to generate an output based on the user query, pass it to an evaluator component, critique the response, identify missing criteria, reformulate execution instructions, and run generation iteratively until criteria are satisfied
- b. A prompt with a generic template with placeholders for `{Query}` and `{Context}`
- c. A prompt that contains rules about not inventing details and saying "I couldn't find this information" but missing evaluation steps
- d. NONE of these prompts are appropriate for a reflex design pattern
- e. A prompt that lists a set of tools but missing the instructions on critiquing its own response

### **Q135.** Which of the following prompts would be the best if you are building an agentic application that implements a planning design pattern?
- a. A prompt that breaks execution down into distinct operational steps: instructing the model to take a user query, decompose it into smaller logical steps, write down a plan, execute each sub-task systematically, monitor intermediate results, and assemble the partial results into a final answer
- b. A generic instruction template with empty execution loops
- c. A prompt that tells the model to use general knowledge without notifying the user when information is missing
- d. NONE of these prompts are appropriate for a planning design pattern
- e. A prompt that tells the model to answer quickly without breaking down the problem

---

## LLMs

### **Q80.** We loaded a pretrained decoder-only transformer (LlamaForCausalLM) from HuggingFace. The model has `Embedding(128256, 2048)` and `lm_head: Linear(in_features=2048, out_features=128256)`. What is the vocabulary size of the model?

```python
LlamaForCausalLM(
  (model): LlamaModel(
    (embed_tokens): Embedding(128256, 2048)
    (layers): ModuleList(
      ...
    )
    (norm): LlamaRMSNorm((2048,), eps=1e-05)
    (rotary_emb): LlamaRotaryEmbedding()
    )
  (lm_head): Linear(in_features=2048, out_features=128256, bias=False)
)
```

- a. 8192
- b. Vocabulary size will vary depending on the length of the prompt
- c. 128256
- d. Vocabulary size is usually fixed at 1,000,000 for all models
- e. 2048 x number_of_heads
- f. Vocabulary size will vary depending on the number of stopwords in the prompt
- g. 512
- h. 2048
- i. 2048 x 128256
- j. More information is needed

### **Q81.** In the same Llama model, what is the "lm_head" component doing?

- a. ALL other options are correct
- b. Projecting the input embedding of a token into the Query vector
- c. Mapping embedding vectors from the last transformer block into logits (to generate a probability distribution over output tokens)
- d. Sampling the next token by redistributing the probability mass over the top k tokens
- e. Merging the heads of an attention layer in order to produce a vector of the same size of the embedding vector

### **Q82.** State-of-the-art LLMs have typically been trained on how much text?
- a. NONE of the other answers are correct
- b. millions of tokens of text
- c. quadrillions of tokens of text
- d. no text, the models are trained on images
- e. thousands of tokens of text
- f. billions of tokens of text
- g. trillions of tokens of text

### **Q83.** State-of-the-art opensource LLMs typically have how many parameters?
- a. hundreds of parameters
- b. NONE of the other answers are correct
- c. millions of parameters
- d. trillions of parameters
- e. tens of parameters
- f. an uncountable number of parameters, since they simply compress all the training data
- g. billions of parameters
- h. thousands of parameters
- i. no parameters, since they make use of non-parametric methods
- j. quadrillions of parameters

### **Q84.** Which of the following statements about current open-source LLM technology (in 2024) is NOT true?
- a. Current open-source LLMs have vocabulary sizes in the tens of thousands
- b. Current open-source LLMs have billions of parameters
- c. Current open-source LLMs have been trained on trillions of tokens of text
- d. Current open-source LLMs contain thousands of transformer layers
- e. ALL of the other options are TRUE
- f. Current open-source LLMs use embeddings with thousands of dimensions

### **Q85.** Which statement about state-of-the-art opensource LLMs is NOT generally true?
- a. LLMs make use of bidirectional transformer architectures
- b. NONE of the other options are correct
- c. LLMs make use of embeddings with thousands of dimensions
- d. LLMs make use of tens to hundreds of layers of transformer blocks
- e. LLMs make use of sub-word tokenisation

### **Q86.** While we don't know the details of OpenAI's GPT-3.5 and GPT-4 models, which of the following is highly likely given their names?
- a. the models make use of Generic Parallel Tokenisers
- b. the models make use of an encoder-decoder architecture
- c. the models use a bidirectional architecture
- d. the models have been trained using Guided Parental Teaching techniques
- e. the models have been trained to perform Generic Pattern Translation
- f. the models contain 3.5 and 4 billion parameters, respectively
- g. NONE of the other answers is correct
- h. the models make use of an autoregressive architecture
- i. the models are 3.5GB and 4GB in size, respectively
- j. the models make use of a noisy autoencoder architecture

### **Q87.** Which of the following statements about content generated by an LLM is obviously FALSE?
- a. NONE of the other options is obviously false
- b. generated content can sometimes be inconsistent with respect to general world knowledge
- c. generated content can sometimes contain lies
- d. generated content can sometimes contain mathematical inaccuracies (e.g. "1+1=3")
- e. generated content can sometimes disagree with the source information provided to the LLM
- f. generated content can sometimes be repetitive
- g. generated content can sometimes be considered offensive

### **Q88.** Do LLMs sometimes generate statements that are factually incorrect? If so, why?
- a. Yes, because LLM stands for Lying Language Model
- b. Yes, because the LLM has been trained to copy human behaviour and humans lie all the time
- c. No, because they have been trained to never tell lies
- d. Yes, because the LLM generates text one token at a time conditioned on previous tokens and there is no guarantee that the resulting text will not contain factual inaccuracies
- e. Yes, because the LLM can often be mistaken in its belief as to what is true and what is false
- f. NONE of the other answers is correct
- g. No, because the reasoning process performed by an LLM checks the truth of all statements before they are generated
- h. No, because like Spock from Star Trek, LLMs are inherently incapable of saying something that isn't true

### **Q89.** Suppose we have an input embedding matrix of a decoder-only transformer. If we swap the vectors for "cat" and "cow" and for "bird" and "dog", and then ask "What sound does the cow make?", what would it likely respond?
- a. Chirp!
- b. An error, since it is not possible to substitute an embedding without messing up the entire forward pass
- c. Meow!
- d. Moo!
- e. Woof!

### **Q90.** Turning an LLM into a Chatbot usually involves:
- a. fine-tuning the model by getting it to talk to itself
- b. NONE of the other options is correct
- c. fine-tuning the model by teaching it to play chess, go, backgammon and other board games
- d. fine-tuning with reinforcement learning from human feedback
- e. increasing the number of layers in the transformer stack
- f. Urban navigation or structural parameters
- g. increasing the dimension of the internal embedding representation

### **Q91.** Reinforcement Learning from Human Feedback is usually used to do what?
- a. evaluate the performance of a pre-trained LLM
- b. train an LLM to understand customer feedback
- c. train an LLM to predict human emotions
- d. turn a pre-trained LLM into a Chatbot
- e. NONE of the other options is correct
- f. reinforce stereotypes held by humans during the training of an LLM

### **Q92.** Telling an LLM to "Take a deep breath and work on this problem step-by-step." after asking it a question is an example of:
- a. an instruction that is not going to have any effect on the question-answering performance of an LLM
- b. NONE of the other answers is correct
- c. zero-shot chain-of-thought prompting
- d. an effective way to waste computational resources
- e. users anthropomorphising chatbots and believing that they are living, breathing entities
- f. meditation and yoga-inspired prompting

### **Q93.** Chain-of-thought prompting of an LLM involves:
- a. providing textual explanations of the reasoning required to calculate an answer when providing examples to an LLM
- b. adding the prompt "chain-of-thought:" before the task description given to the LLM
- c. chaining together multiple LLMs in series to solve a task by combining their individual reasoning capabilities
- d. calling an LLM multiple times with a chain of prompts that break down the task into smaller sub-tasks
- e. NONE of the other options is correct

### **Q94.** Prompting a chatbot in a certain way so as to cause it to respond in an unintended manner and operate outside of its intended operating conditions is usually referred to as:
- a. re-schooling the chatbot
- b. NONE of the other options is correct
- c. violentizing the chatbot
- d. delinquentizing the chatbot
- e. denaturing the chatbot
- f. It is NOT POSSIBLE to force a chatbot to respond in an unintended manner
- g. retasking the chatbot
- h. jailbreaking the chatbot

### **Q95.** Write a few-shot prompt for extracting sentiment and aspect information from hotel guest feedback using an LLM. The sentiment values are: positive, negative, neutral. The aspects are: cleanliness, friendliness (of staff), location, breakfast. Apply the prompt to the following feedback: "totally loved the place, particularly the breakfast smorgasboard". *(Open-ended question)*

---

## Topic 8: Open-source LLMs

### **Q96.** Is it possible to generate text from a 7 billion parameter LLM on a computer with a 12GB GPU card?
- a. Yes, providing we quantise the parameters of the model to say 8-bits while loading it
- b. No, LLMs can't be used to generate text, only to classify it
- c. Yes, providing we make use of LoRA (Low Rank Adapter) adapters when loading the model
- d. No, each parameter requires at least 2 bytes (16 bits) in half precision format, so we would need at least 14GB of video memory
- e. No, the gradients of the model would require at least as much memory as is needed to store the parameters
- f. No, to run such a big model we need access to a TPU
- g. Insufficient information was provided to answer the question

### **Q97.** If we apply 4-bit quantisation when loading a Mistral-7B LLM on a GPU, approximately how much video RAM would be needed to store the parameters of the model?
- a. 7 TB
- b. 350 MB
- c. 3.5 TB
- d. 3.5 GB
- e. 14 GB
- f. 28 TB
- g. NONE of the other options are correct
- h. 7 GB
- i. 700 MB
- j. 1.4 GB
- k. 28 GB

### **Q98.** Which technique employed in modern LLMs has allowed them to ingest much longer prompts than was possible before?
- a. grouped self-attention
- b. sliding window attention
- c. mixture of experts
- d. rotational positional embeddings
- e. NONE of the mentioned techniques have resulted in larger effective context window sizes
- f. combination of linear and non-linear activations in MLP layers

### **Q99.** Which statement about contemporary LLM architectures is NOT true?
- a. Causal attention is used to avoid a token from attending to future tokens in the sequence
- b. Softmax activation is usually applied within each self-attention layer to normalise the attention matrix
- c. Flash-attention is an approximate attention technique that reduces memory footprints at the cost of significantly lower accuracy
- d. Rotary Position Embeddings are applied to input embeddings before calculating queries and keys
- e. Models often make use of a combination of linear and non-linear activations in the MLP layers to improve performance
- f. The use of mixture-of-experts architectures has allowed for efficient training of larger models with more parameters

### **Q100.** Given a Llama model summary with `input_layernorm` and `post_attention_layernorm` in each decoder layer, what is the `post_attention_layernorm` doing?
```python
LlamaForCausalLM(
  (model): LlamaModel(
    (embed_tokens): Embedding(128256, 2048)
    (layers): ModuleList(
      (0-15): 16 x LlamaDecoderLayer(
        (self_attn): LlamaAttention(
          (q_proj): Linear(in_features=2048, out_features=2048, bias=False)
          (k_proj): Linear(in_features=2048, out_features=512, bias=False)
          (v_proj): Linear(in_features=2048, out_features=512, bias=False)
          (o_proj): Linear(in_features=2048, out_features=2048, bias=False)
        )
        (mlp): LlamaMLP(
          (gate_proj): Linear(in_features=2048, out_features=8192, bias=False)
          (up_proj): Linear(in_features=2048, out_features=8192, bias=False)
          (down_proj): Linear(in_features=8192, out_features=2048, bias=False)
          (act_fn): SiLU()
        )
        (input_layernorm): LlamaRMSNorm((2048,), eps=1e-05)
        (post_attention_layernorm): LlamaRMSNorm((2048,), eps=1e-05)
      )
    )
    (norm): LlamaRMSNorm((2048,), eps=1e-05)
    (rotary_emb): LlamaRotaryEmbedding()
  )
  (lm_head): Linear(in_features=2048, out_features=128256, bias=False)
)
```

- a. NONE of the other answers are correct
- b. normalizing the output of the self-attention layer before adding it to the residual embedding
- c. normalizing the initial token embeddings on input to the network
- d. normalizing the residual embedding before feeding it into the MLP component
- e. normalizing the residual embedding before feeding it into the self-attention component
- f. subtracting the output of the self-attention component from the output of the MLP component before adding it back to the residual
- g. normalizing the attention scores within the self-attention component

---

## Topic 9: Retrieval Augmented Generative (RAG) Models

### **Q101.** Low Rank Adaptation (LoRA) is used for:
- a. training a rank-learning algorithm to rerank documents within a search engine
- b. NONE of the other options are valid
- c. fine-tuning LLMs with less computational resources
- d. representing documents based on a few main topics
- e. adapting the loss function during model training to reduce its rank
- f. ranking text retrieval results to reduce topical variation

### **Q102.** Low Rank Adaptation (LoRA) is a technique in which we:
- a. estimate word embedding vectors using low rank matrix factorisation
- b. adapt the loss function during training by reducing its rank
- c. train a rank-learning algorithm to rerank retrieved documents in a RAG model
- d. NONE of the other options are correct
- e. introduce a small set of new parameters in order to fine-tune an LLM
- f. approximate a document-term matrix with a low-rank factorisation to discover important topics

### **Q103.** Further training an LLM to improve its reasoning ability is usually referred to as:
- a. instruction tuning for tool calling
- b. NONE of the other answers is correct
- c. reasoning training
- d. high schooling the LLM
- e. logic learning
- f. hyper-reasoning
- g. test-time compute scaling
- h. brainfication

### **Q104.** What types of problems are often used to train LLMs to improve their reasoning abilities?
- a. chess games that have been started, but not completed, by grand masters
- b. NONE of the other answers are correct
- c. ethical dilemmas such as the runaway trolley problem
- d. high school mathematics problems where the correct answers are known but the reasoning required isn't
- e. Millennium Prize problems such as the Riemann Hypothesis
- f. philosophical problems such as the question of free will
- g. children's games like rock-paper-scissors

### **Q105.** In the context of LLMs, test-time compute scaling usually refers to the process of:
- a. NONE of the other answers is correct
- b. scaling up the testing of an LLM to include much harder problems
- c. increasing the number of tasks included in the test dataset used to evaluate the LLM
- d. training an LLM to spend more time "thinking" and thereby improve its reasoning ability
- e. balancing the amount of data used for training and testing an LLM so as to optimise performance for a given number of model parameters
- f. deploying an LLM on much faster computational resources

### **Q106.** According to the LLM prompt below, how many different tools are available for the agent to make use of?

> "You are an assistant that has access to the following set of tools.
> Here are the names and descriptions for each tool:
> **exponentiate**(base: float, power: float) -> float - computes base raised to the power
> **compound_interest**(principal: float, rate: float, years: float) -> float - applies interest rate to principal for set number of years
> **play_radio_tool**() - starts the radio
> **pause_radio_tool**() - pauses the radio if it is playing
> **increase_radio_volume_tool**() - increases the volume of the radio if it is playing
> **decrease_radio_volume_tool**() - decreases the volume of the radio if it is playing
> **search_tool5**(query: str) -> list[str] - uses the query to perform a web search and return a list of relevant documents
> **translate_tool6**(input: str, language: str) -> str - returns input translated into the language
> Given the user input, return the name and input of the tool to use.
> Return your response as a JSON blob with 'name' and 'arguments' keys.
> The `arguments` should be a dictionary, with keys corresponding to the argument names and the values corresponding to the requested values.
> If the tool takes no arguments, provide an empty dictionary."

- a. 2 tools
- b. No tools are provided in the prompt
- c. 5 tools
- d. 6 tools
- e. 4 tools
- f. 7 tools
- g. 8 tools
- h. 10 tools
- i. 1 tool
- j. NONE of the other answers is correct
- k. 3 tools

### **Q107.** Which of the following prompts would be the best if you are building a RAG (Retrieval Augmented Generation) application?
- a. A prompt that uses retrieved context, tells the model to answer from it when possible, to clearly indicate when extrapolating beyond context, never invent details contradicting context, and say "I couldn't find this information" when needed — including both `{retrieved_documents}` and `{user_query}` placeholders
- b. A generic instruction-following template with empty `{Instruction}`, `{Input}`, and `{Response}` placeholders
- c. A prompt that uses retrieved context but tells the model to use general knowledge without notifying the user when context is insufficient — including `{retrieved_documents}` but missing `{user_query}`
- d. NONE of these prompts are appropriate for a RAG application
- e. A prompt with rules about not inventing details and saying "I couldn't find this information" — but missing the `{retrieved_documents}` placeholder entirely

---

## Topic 10: Speech Detection & Generation. Processing Spoken Dialog

### **Q108.** Text normalisation is needed for a text-to-speech system in order to:
- a. expand numeric values like "123" into word form: "one hundred and twenty three"
- b. scale the length of the sentence embedding to 1
- c. None of the other options are correct
- d. scale the amplitude of the output audio signal to have an average of 1dB

### **Q109.** When you ring your mobile phone operator and try to find your way through their voice interaction menu in order to make changes to your account settings, you are probably talking to:
- a. a wizard-of-oz style experiment
- b. a task-oriented dialog system
- c. NONE of the other options
- d. a retrieval-based chatbot
- e. a deep hierarchical isotropic chatbot
- f. an open domain chatbot

### **Q110.** Your company wants to build a voice interactive system to control a washing machine. The system handles fabric type, cycle duration, temperature, spin cycle, and start delay. The machine has cameras and a weight sensor. What tools and data would you need, and how would you go about developing the system? *(Open-ended question)*

### **Q111.** Which of the following statements about human speech and hearing is NOT true?
- a. Most humans can hear frequencies up to 100 kHz
- b. Human hearing is sensitive over a broad range (many orders of magnitude) of amplitude values
- c. Humans are sensitive to multiplicative rather than absolute changes in pitch
- d. All of the other answers are true
- e. Speech is generated by changing (restricting) the airflow through the vocal tract

### **Q112.** Which of the following statements about Wav2vec (2020) and Whisper (2022) is true?
- a. Wav2vec (2020) applies a 1-dimensional convolutional Neural Network directly to the audio signal
- b. Whisper (2022) makes use of a Mel spectrogram of the audio signal
- c. They are both text-to-speech systems based on a Transformer architecture
- d. ALL of the other options are true

### **Q113.** Which, if any, of the following techniques is NOT used to produce a spectrogram for analysing audio signals? 
- a. All of the other techniques are used
- b. Dimensionality reduction (t-SNE)
- c. Pre-emphasis filtering
- d. Fast Fourier Transform (FFT)
- e. Hamming windows on overlapping time-segments

### **Q114.** Some people speak faster than others. If a phoneme detection system is trained on time intervals for fast speakers, slower speakers will produce many repeated phonemes. How might we BEST overcome this problem when building a speech transcription system?
- a. get everyone to speak at exactly the same speed
- b. just remove all repeated characters from the output text
- c. None of the other options are correct
- d. use a variable sized time window to detect the phoneme (and learn to predict its size)
- e. learn a sequence-to-sequence model to directly convert from longer sequences to shorter ones

---

## Topic 11: Evaluating NLP

### **Q115.** The term "LLM-as-a-Judge" refers to the use of an LLM to:
- a. judge whether a defendant is guilty as charged in a court of law
- b. NONE of the other answers is correct
- c. score candidates for a job based on their résumés
- d. replace all lawyers and courtrooms with automated judicial techniques
- e. collect ground truth labels for training classifiers by scraping the internet
- f. self-censor its output to prevent it making insensitive or offensive statements to users
- g. evaluate correctness, quality or relevance of generated content for an NLP task
- h. judge entertainers in a talent show

### **Q116.** BLEU-4 is:
- a. a question-answering dataset, where each question has exactly 4 multiple choice options
- b. a word embedding that maps tokens into four-dimensional vectors
- c. an open-source LLM with approximately 4 billion parameters
- d. a text evaluation measure that compares strings based on unigrams, bigrams, trigrams and 4-grams
- e. NONE of the other options is correct
- f. a measure of search result quality that combines the output of four different retrieval measures

### **Q189.** In evaluating machine translation or text generation, how does the ROUGE metric differ fundamentally from BLEU?
- a. BLEU is calculated manually by human judges while ROUGE is entirely algorithmic
- b. BLEU focuses primarily on precision (how many generated n-grams match the reference), whereas ROUGE focuses primarily on recall (how many reference n-grams are successfully generated)
- c. ROUGE can only process character-level inputs while BLEU requires full paragraph vectors
- d. BLEU measures structural parse tree similarities exclusively
- e. NONE of the other options are correct

### **Q160.** Which of the following evaluations represents a "non-parametric" approach?
- a. t-test
- b. ANOVA
- c. Wilcoxon signed-rank test
- d. F-test
- e. NONE of the other options are correct

---

## Unmapped Original Content Topics


### **Q143.** Why are Natural Language Processing (NLP) techniques important?
- a. are important because text can influence public opinion
- b. are important because mining it can lead to new scientific discoveries
- c. involve techniques for extracting useful knowledge from textual data
- d. concern the computational analysis, interpretation, and production of natural language in either written or spoken form
- e. are important because text is pervasive
- f. ALL the other statements are true

### **Q144.** Which of the following tasks would NOT usually be considered a Natural Language Processing task?
- a. automatically translating data from one natural language to another
- b. automatically identifying the type of plant in an image taken on a mobile phone
- c. automatically fact-checking statements made by a politician
- d. automatically summarising an article written by a scientist
- e. automatically determining the author of a piece of text
- f. automatically determining the emotions being expressed by a speaker

### **Q145.** Sentences in natural language can often be ambiguous (for example "I made her duck" could have multiple interpretations), because:
- a. the objects discussed in the text (described by noun phrases) might be underspecified
- b. ALL of the other reasons are valid
- c. the same word can take on different lexical categories (e.g. "duck" might be a noun or a verb) depending on the context
- d. the same word can take on different meanings (e.g. "to make" might mean "to cook" something or "to force someone to do" something) depending on the context

### **Q146.** The sentence "Colourless green ideas sleep furiously." is an example of a phrase that:
- a. cannot be POS tagged
- b. would likely be generated by a Large Language Model
- c. makes no sense, but is grammatically correct
- d. contains multiple out-of-vocabulary terms
- e. NONE of the other options is correct


### **Q182.** Fine-tuning a pre-trained language model on a curated dataset of instructions and responses is called:
- a. Masked Language Pre-training
- b. Supervised Fine-Tuning (SFT) / Instruction Tuning
- c. Contrastive Image-Text Training
- d. Random Walk Optimization
- e. NONE of the other options are correct

### **Q183.** What is a key risk of over-training a model during the fine-tuning phase on a very narrow task?
- a. The vocabulary size of the tokenizer might shrink unexpectedly
- b. Catastrophic Forgetting, where the model loses its generalized capabilities and performance on broader, un-tuned domains drops sharply
- c. The context window might expand beyond hardware capacity limits
- d. The model will convert from an autoregressive setup to a bidirectional encoder
- e. NONE of the other answers is correct

### **Q184.** What does "Parameter-Efficient Fine-Tuning" (PEFT) aim to achieve?
- a. to speed up inference by removing layers from the transformer architecture
- b. to adapt a large model to specific tasks by updating or adding only a minute fraction of total parameters, lowering computational and storage costs
- c. to automatically rewrite prompt formatting matrices without updating weights
- d. to increase parameter sizes past trillions without inflating VRAM targets
- e. NONE of the other answers is correct

### **Q185.** In a Mixture of Experts (MoE) model architecture, the "Routing Network" is responsible for:
- a. allocating data packets to alternative physical GPU nodes across networks
- b. dynamically directing each input token to the most appropriate subset of specialized expert layers (MLPs) for processing
- c. parsing sentence trees into distinct part-of-speech dependencies
- d. retrieving text blocks from external vector database indices during RAG pipelines
- e. NONE of the other options is correct

### **Q186.** What is the primary function of a "Vector Database" in modern semantic search architectures?
- a. to host raw text documents alphabetically for quick index access profiles
- b. to store dense high-dimensional embedding vectors and perform rapid approximate nearest neighbor (ANN) similarity calculations
- c. to optimize matrix calculations within the multi-head attention stack
- d. to execute regular expression string patterns over raw text files
- e. NONE of the other options are correct

### **Q187.** What is "Hallucination" in the context of Large Language Models?
- a. when the model throws an out-of-memory error during execution steps
- b. when the model generates content that is syntactically fluent but factually fabricates or contradicts source context data
- c. when the tokenizer maps subword fragments to un-indexed characters
- d. when rotary position systems cause attention scores to loop indefinitely
- e. NONE of the other choices is correct

### **Q188.** What design pattern is characterized by providing an LLM with access to external tools and allowing it to iteratively decide actions, observe results, and reason until a final goal is met?
- a. Pipeline Pattern
- b. Agentic Loop (e.g., ReAct Framework)
- c. Classification Chain
- d. Inverted Index Mapping
- e. NONE of the other answers is correct


### **Q190.** What is the primary goal of "Model Distillation" in natural language processing?
- a. to combine multiple open-source LLMs into a massive unified mixture of experts
- b. to train a smaller, more efficient "student" model to replicate the behaviors, outputs, or probability distributions of a larger "teacher" model
- c. to clean a raw text crawl by stripping out markup, punctuation, and low-frequency terms
- d. to dynamically expand context windows during token generation loops
- e. NONE of the other answers is correct

### **Q191.** What does a "Steering Vector" do when applied to a Large Language Model during inference?
- a. It alters physical hardware configurations dynamically to maximize prompt ingest rates
- b. It adds a specific activation bias vector directly into internal layers during the forward pass to subtly bias the model's behavioral tone, style, or topical focus
- c. It forces the model to select the absolute maximum index in the tokenizer vocabulary matrix
- d. It acts as an inverted lexical index inside vector storage frameworks
- e. NONE of the other options are correct

### **Q192.** What is the purpose of an XAI technique that extracts "Attention Maps" from a Transformer model?
- a. to measure the precise thermal temperature parameters of hardware cores
- b. to visualize and audit which specific tokens or contextual elements the model is weighting most heavily when processing or generating a given output token
- c. to automatically eliminate redundant hidden weights across feed-forward blocks
- d. to calculate exact analytical derivatives without running backpropagation parameters
- e. NONE of the other options are correct

### **Q193.** A system that translates an audio recording of a person speaking into an equivalent written text transcript is performing:
- a. Text-to-Speech (TTS) synthesis
- b. Automatic Speech Recognition (ASR) / Speech-to-Text (STT)
- c. Conversational Analysis parsing
- d. Semantic Language Modeling
- e. NONE of the other choices is correct

### **Q194.** What is the purpose of a "Mel Spectrogram" in spoken language applications?
- a. to store text characters using a highly compressed 4-bit binary vocabulary structure
- b. to represent the power spectrum of an audio signal over time, with frequencies transformed to match human non-linear pitch perception scales
- c. to trace semantic lineage dependencies across multi-turn user prompt history files
- d. to act as a parameter-efficient fine-tuning adapter within decoder stacks
- e. NONE of the other answers is correct

---

## A Joke

### Q200. Which of the following techniques for identifying students attempting to cheat by using ChatGPT during an exam would NOT be effective?
- a. Doing nothing, since ChatGPT is morally obliged not to help them during an exam, and would get the answer wrong anyway
- b. All of the other options are effective approaches
- c. Hiding instructions in very small white font within the question text, so that it is copied into the ChatGPT prompt by the student
- d. Training a model to determine whether the text entered by the student was produced by ChatGPT
- e. Forcing students to use a safe browser so that they can't access ChatGPT during the exam
