## A Trainable Document Summarizer Using Bayesian Classifier Approach
Author: Aditi Sharan, Hazra Imran, Manju Joshi
year: 2008


### Notes

<mark class="customZot-Yellow ">Table 1: Scores of the document f1 Edmundson feature f2 Luhn Feature f3 Location feature f4 Cue phrase feature f5 Title Feature f6 First sentence Feature f7 Sentence Length Cut-off Feature f8 Occurrence of Proper noun 3.3 Bayesian classifier approach for Document Summarization This section quickly reviews the basis of the Naïve Bayes classifier. We have implemented a Bayesian classifier that computes the probability that a sentence in a source document should be included in a summary. For each sentence s, the probability of s being included in the summary is calculated based on the k given features Fj: j=1....k which can be expressed using the Bayers rule as follows: P(s Є S | F1, F2....Fk) = P (F1, F2 ....Fk) | s Є S) P (s Є S) P (F1, F2 ....Fk) Assuming statistical independence of the features P(s S | F1, F2....Fk) = k j=1 P (Fj | s S) P (s S) k j=1 P (Fj) P (s Є S) is a constant and P (Fj | s Є S) and P (Fj) can be estimated directly from the training set by counting occurrences. This yields a simple Bayesian classification function that assigns for each sentence s a score which can be used to select sentences for inclusion in the summary. Once the classifier has been trained, it can be used as a tool to filter sentences in any document and determine whether each sentence should be included in the summary or not.</mark> ([5](zotero://open-pdf/library/items/CJLXBQRN?page=5&annotation=VIHEY5Y8))

   ![[Sources/Images/sharanTrainableDocumentSummarizer2008/image-6-x309-y610.png]]