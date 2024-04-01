## Automatic Text Summarization Using a Machine Learning Approach
Author: Joel Larocca Neto, Alex A. Freitas, Celso A. A. Kaestner
year: 2002


### Notes

<mark class="customZot-Yellow ">For the next features an approximate argumentative structure of the text is employed. It is a consensus that the generation and analysis of the complete rethorical structure of a text would be impossible at the current state of the art in text processing. In spite of this, some methods based on a surface structure of the text have been use</mark> ([4](zotero://open-pdf/library/items/4XJI8M3H?page=4&annotation=VUUMUPZI))

 
<mark class="customZot-Yellow ">to obtain good-quality summaries [23], [24]. To obtain this approximate structure we first apply to the text an agglomerative c lustering algorithm. The basic idea of this procedure is that similar sentences must be grouped together, in a bottom-up fashion, based on their lexical similarity. As result a hierarchical tree is produced, whose root represents the entire document. This tree is binary, since at each step two clusters are grouped. Five features are extracted from this tree, as follows: (h) Depth in the tree. This feature for a sentence s is the depth of s in the tree. (i) Referring position in a given level of the tree (positions 1, 2, 3, and 4). We first identify the path form t he root of the tree to the node containing s, for the first four depth levels. For each d epth level, a feature is assigned, according to the direction to be taken in order to follow the path from the root to s; since the argumentative tree is binary, the possible values for each position are: left, right and none, the latter indicates that s is in a tree node having a depth lower than four.</mark> ([5](zotero://open-pdf/library/items/4XJI8M3H?page=5&annotation=N8WFVZMG))

  
>Доволі цікавий вибір фічі
  ![[Sources/Images/netoAutomaticTextSummarization2002/image-7-x121-y304.png]]
<mark class="customZot-Yellow ">We can draw the following conclusions from this experiment: (1) the values of precision and recall for all the methods are significantly higher with the rate of 20% than with the compression rate of 10 %; this is a expected result, since the larger the compression rate, the larger the number of sentences to b e selected for the summary, and then the larger the probability that a sentence selected by a summarizer matches with a sentence belonging to the extractive summ ary; (2) the best results were obtained by our trainable summarizer with Naive Bayes classifier for both compression rates; using the same features, but with the C4.5 as classifier, the obtained results were poor: the results are similar to the First-Sentences and Word Summarizer baselines.</mark> ([7](zotero://open-pdf/library/items/4XJI8M3H?page=7&annotation=V57T54ZS))

  
>висновок щодо відсотку взяття речень

<mark class="customZot-Yellow ">The test database was composed o f 30 documents, selected at random from the original document base. The manual reference summaries were produced by a human judge – a professional English teacher with many years of experience –specially hired for this task. For the compression rates of 10 % and 20% the same four summarizers of the first experiment were compared. The obtained results are presented in Table 2.</mark> ([8](zotero://open-pdf/library/items/4XJI8M3H?page=8&annotation=M84M65T9))

   ![[Sources/Images/netoAutomaticTextSummarization2002/image-8-x119-y385.png]]