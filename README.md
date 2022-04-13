
# **Topic Modeling using LDA** 
## Table of Content:

 - [Project Overview](#overview)
 - [Tools used](#installation)
 - [Approach](#Approach)
 - [Results and Findings](#results)
 - [Final thoughts](#get_start)
 
<a name="overview"></a>
## Project Overview 
**A medical-related dataset, containing 5k articles. It is required to map each document to the top 3 topics it belongs to and show the probability score for each topic. I solved this problem using latent Dirichlet allocation (LDA) Genism implementation.**

<a name="installation"></a>
## Tools used:

*	Jupyter notebook
*	Python
*	NLTK
*	Spacy
*	Genism
*	Pandas
*	Matplotlib
*	Numpy

<a name="Approach"></a>
## The Approach: 

*	Data Preprocessing: this step is used to prepare the raw text for feature extraction. The process included:


	* Removing Punctuation and lowering case all words.
	* Removing stop words that do not affect the overall meaning of a sentence such as he, she, etc...
	* Lemmatization to return words to their root meaning following English dictionary such as (ran, run), (are, be), and stemming that does the same thing following an algorithm (focus, focu), (association, associ).
	        
		
*	Feature extraction: Machine learning algorithms do not deal with text it only understands numbers. So that is why the step of converting a document to numbers with meaningful features is crucial for training the algorithm. This can be done by :


	* Converting the training set we have to a dictionary that tells how many times a word occurred in the dataset.

	* Creating a bag of words BOW that tells how many times a word occurred within a document.

	* TF-ID that instead of only counting the number of occurrences, it takes into account the frequency of occurrence of each word in a document. Hence, it tells
	how important a specific word is to a document.
	
*	Model training and choosing the optimal number of topics. I used topic coherence to evaluate the performance of the LDA following the same technique in this paper. Then, A CSV file is loaded including the assignment of each document to the top three topics it may belong to using a probability score to order them.

*	Results Loading ( Graphs, CSVs, and the final model )
*	
<a name="results"></a>
 ## Results and Findings:
 
After training 50 models using the number of topics as the only variable parameter and storing
the coherence score of each model, I found that the number of topics that has the highest
coherence score is 4. The results are illustrated in the following graph.   


![](https://github.com/sam1o1/topic_modeling_using_lda/blob/main/results/num_of_topics.png?raw=true)

Among the three topics that a document may belong to, the following graph shows the first
dominant topic among all documents.

![](https://github.com/sam1o1/topic_modeling_using_lda/blob/main/results/first_top_topic.png?raw=true)

<a name="get_start"></a>
## Final Thoughts
I think if I included more feature extraction such as adding tri-grams and building the model Without stemming, this may result in a better performance. The problem with stemming is that sometimes it results in some words that are not human-friendly or actual English vocabulary.


## Licensing and Authors

Author : Eslam Abdelghany

Email: eslam322_1@hotmail.com

 
 




