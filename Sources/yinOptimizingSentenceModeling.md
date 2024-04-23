## Optimizing Sentence Modeling and Selection for Document Summarization
Author: Wenpeng Yin, Yulong Pei
year: Error: `format` can only be applied to dates. Tried for format object


### Notes
  ![[cnn.png]]
<mark class="customZot-Yellow ">Input Layer: A sentence with s words: w0, w1, · · · , ws−1. Each word wi is denoted by an initialized vector wi ∈ Rd (“300” in Figure 1 denotes representation of dimension 300).</mark> ([2](zotero://open-pdf/library/items/MD3RXBHR?page=2&annotation=VCDC83SP))

 
<mark class="customZot-Yellow ">Convolution Layer: a convolution layer uses sliding f ilters to extract features of local phrases in the sentence.</mark> ([2](zotero://open-pdf/library/items/MD3RXBHR?page=2&annotation=W97BQR9A))

 
<mark class="customZot-Yellow ">Max-pooling Layer: Based on representations of all regional phrases, max-pooling layer extracts the maximum value from each dimension to form sentence representation x ∈ Rd.</mark> ([2](zotero://open-pdf/library/items/MD3RXBHR?page=2&annotation=XEXDCHYQ))

 
<mark class="customZot-Yellow ">In order to train the CNN in an unsupervised scheme, we form a n-gram language model by element-wisely averaging sentence representation and the representations of context words to predict the next word, as depicted “average” in Figure 1. This process resembles the CBOW scheme in word2vec [Mikolov et al., 2013] which has no global sentence features to help prediction, resembles also the PV-DM model in [Le and Mikolov, 2014] while our sentence representation is derived by CNN.</mark> ([3](zotero://open-pdf/library/items/MD3RXBHR?page=3&annotation=ZVCT2HJG))

 
<mark class="customZot-Yellow ">DivSelect: Optimizing Sentence Selection</mark> ([3](zotero://open-pdf/library/items/MD3RXBHR?page=3&annotation=GS7IIKLW))

   ![[Sources/Images/yinOptimizingSentenceModeling/image-3-x54-y142.png]]
<mark class="customZot-Yellow ">where α is a positive regularization parameter that defines the trade-off between the two terms, i.e., prestige and diversity, and pi is the ith entry of prestige vector p</mark> ([3](zotero://open-pdf/library/items/MD3RXBHR?page=3&annotation=7SVUV66H))

   ![[algo.png]]  ![[duc2002res.png]]  ![[duc 2004.png]]  ![[similarity.png]]