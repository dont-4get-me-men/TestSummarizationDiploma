## SummaRuNNer: A Recurrent Neural Network based Sequence Model for Extractive Summarization of Documents
Author: Ramesh Nallapati, Feifei Zhai, Bowen Zhou
year: 2016


### Notes

<mark class="customZot-Yellow ">We use a GRU based Recurrent Neural Network (Chung et al. 2014) as the basic building block of our sequence classifier</mark> ([2](zotero://open-pdf/library/items/SM2WYSAY?page=2&annotation=8PDBZ63Z))

 
<mark class="customZot-Yellow ">e Hadamard product. Our model consists of a two-layer bi-directional GRURNN, whose graphical representation is presented in Figure 1. The first layer of the RNN runs at the word level, and computes hidden state representations at each word position sequentially, based on the current word embeddings and the previous hidden state. We also use another RNN at the word level that runs backwards from the last word to the first, and we refer to the pair of forward and backward RNNs as a bidirectional RNN. The model also consists of a second layer of bi-directional RNN that runs at the sentence-level and accepts the average-pooled, concatenated hidden states of the bi-directional word-level RNNs as input. The hidden states of the second layer RNN encode the representations of the sentences in the document. The representation of the entire document is then modeled as a non-linear transformation of the average pooling of the concatenated hidden states of the bi-directional sentence-level RNN, as shown below.</mark> ([2](zotero://open-pdf/library/items/SM2WYSAY?page=2&annotation=BLW8KQ8Y))

   ![[summarunner neural.png]]
<mark class="customZot-Yellow ">Extractive Training In order to train our extractive model, we need ground truth in the form of sentence-level binary labels for each document, representing their membership in the summary. However, most summarization corpora only contain human written abstractive summaries as ground truth. To solve this problem, we use an unsupervised approach to convert the abstractive summaries to extractive labels. Our approach is based on the idea that the selected sentences from the document should be the ones that maximize the Rouge score with respect to gold summaries. Since it is computationally expensive to find a globally optimal subset of sentences that maximizes the Rouge score, we employ a greedy approach, where we add one sentence at a time incrementally to the summary, such that the Rouge score of the current set of selected sentences is maximized with respect to the entire gold summary . We stop when none of the remaining candidate sentences improves the Rouge score upon addition to the current summary set. We return this subset of sentences as the extractive ground-truth, which is used to train our RNN based sequence classifier.</mark> ([3](zotero://open-pdf/library/items/SM2WYSAY?page=3&annotation=HJEG7HFU))

   ![[results.png]]  ![[cnn daily resulta.png]]