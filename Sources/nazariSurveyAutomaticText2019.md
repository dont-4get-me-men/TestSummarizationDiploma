Year: 2019
Authors: N. Nazari, M. A. Mahdavi


Title:: A survey on Automatic Text Summarization
URL: https://jad.shahroodut.ac.ir/article_1189.html
Zotero Link: [Full Text PDF](zotero://select/library/items/87W2UNS9)




> Cue phrases: this feature mentions that the presence or absence of some cue words or phrases such as "as a result," "for example," and "as a matter of fact" indicates the importance of the sentences that include these phrases. 2. Title words: this feature predicts that words appearing in the title of a document are immediately relevant to the concepts outlined in the text. Therefore, these words are viewed as a factor to identify the important sentence. 3. Sentence location: this feature indicates that the location of a sentence in the paragraph reveals its importance to the topic of the paragraph. For instance, sentences that occur in the initial part of a paragraph carry more information than the rest of the paragraph. Therefore, initial sentences of each paragraph are potentially relevant candidates for sentence selection in a document summary.
> 
> 
> Statisical method



> 3.2. Machine learning method The idea behind machine learning is to use a training set of data to train the summarization system, which is modeled as a classification problem. Sentences are classified into two groups: summary sentences and non-summary sentences [24]. The probability of choosing a sentence for a summary is estimated according to the training document and extractive summaries [25]. Some of the common machine learning methods used for text summarization are naïve Bayes, artificial neural network, and fuzzy logic [26, 27].
> 
> 


> 3.3. Semantic-based method When it comes to summarization, statistical features are not all effective across the board because some features depend on the specific format and the writing style of the documents [34]. For example, in title word, the problem is that a document may not have a title. It may also happen that all the frequent words are not as important as lesser frequent words, in which case, ignoring words with less occurrence would provide an unqualified summary. Semantic-based methods identify the relationship between words and sentences by use of a thesaurus, part-ofspeech tagging, grammar analysis, and selection of meaningful sentences to generate summary [35]. Various techniques like lexical chain, clustering, and graph-based methods have been developed in this approach, which will be explained in the following sections.
> 
> 
> 3.3.2. Clustering method



> 3.3.1. Lexical chain method The lexical chain is a sequence of words in a document that are semantically related to one another. This method includes three steps, text segmentation, lexical chain identification, and finally, finding the strongest lexical chain for sentence extraction [36].
> 
> 


> In a clustering method, similar textual units (such as words, sentences or paragraph) are clustered together to identify the common information between them [39].
> 
> 


> 3.3.3. Graph-based method In the field of natural language processing, graphs are used to display the structure of the text and the connection between sentences. Sentences are represented as a node, and the relation between sentences are depicted by edges [43]
> 
> 


> 3.4.1. Particle swarm optimization The particle swarm optimization algorithm is an evolutionary one, which has been introduced for solving an optimization problem [54]. This algorithm is based upon the social movement of birds, and starts with a population of birds to discover the search space.
> 
> 


> The first entails a pre-processing on input document, then a score is assigned to a sentence by the weighting method. Afterward, the similarity between sentences and keyword is obtained using a similarity matrix. Then the cuckoo search optimization algorithm is applied to extract the important sentences, which include five steps [61]: 1. The CSOA parameters are initialized; 2. The sentences are assigned to birds randomly; 3. The assessment of birds is done based on cost function; 4. The position of birds is updated; Figure 2. Movement of a cuckoo toward goal habitat [64]. Group 2 Group 3 Goal point Group 1 d New habitat φ
> 
> 
> Cuckoo optimization algorithm



> Mahdavi & Nazari/ Journal of AI and Data Mining, Vol 7, No 1, 2019. 130 5. The end condition of loops is checked, if it is satisfied, the algorithm is finished; otherwise, return to step 3.
> 
> 


> 

