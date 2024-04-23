## Extractive Summarization using Continuous Vector Space Models
Author: Mikael Kågebäck, Olof Mogren, Nina Tahmasebi, Devdatt Dubhashi
year: 2014


### Notes

<mark class="customZot-Yellow ">The aim is then to find a summary that maximizes diversity of the sentences and the coverage of the input text.</mark> ([2](zotero://open-pdf/library/items/CBMFGCQ8?page=2&annotation=C5WQMVGR))

 
<mark class="customZot-Yellow ">F(S) = L(S) + λR(S) where S is the summary, L(S) is the coverage of the input text, R(S) is a diversity reward function. The λ is a trade-off coefficient that allows us to define the importance of coverage versus diversity of the summary. In general, this kind of optimization problem is NP-hard, however, if the objective function is submodular there is a fast scalable algorithm that returns an approximation with a guarantee</mark> ([2](zotero://open-pdf/library/items/CBMFGCQ8?page=2&annotation=HZPBMKQL))

   ![[Sources/Images/kagebackExtractiveSummarizationUsing2014/image-3-x293-y573.png]]
<mark class="customZot-Yellow ">An auto-encoder (AE) (Hinton and Salakhutdinov, 2006), see Fig. 3, is a type of FFNN with a topology designed for dimensionality reduction</mark> ([3](zotero://open-pdf/library/items/CBMFGCQ8?page=3&annotation=9H62G8NB))

   ![[Sources/Images/kagebackExtractiveSummarizationUsing2014/image-4-x56-y545.png]]
<mark class="customZot-Yellow ">Continuous distributed vector representation of words, also referred to as word embeddings, was first introduced by Bengio et al. (2003). A word embedding is a continuous vector representation that captures semantic and syntactic information about a word. These representations can be used to unveil dimensions of similarity between words, e.g. singular or plural.</mark> ([4](zotero://open-pdf/library/items/CBMFGCQ8?page=4&annotation=GHYPD492))

   ![[Sources/Images/kagebackExtractiveSummarizationUsing2014/image-5-x63-y378.png]]
<mark class="customZot-Yellow ">An unfolding recursive auto-encoder (RAE) is used to derive the phrase embedding on the basis of a binary parse tree. The unfolding RAE was introduced by Socher et al. (2011) and uses two RvNNs, one for encoding the compressed representations, and one for decoding them to recover the original sentence, see Figure 6.</mark> ([5](zotero://open-pdf/library/items/CBMFGCQ8?page=5&annotation=H4KPPTF6))

   ![[RAE.png]]  ![[rouge-1.png]]  ![[rouge-2.png]]  ![[rouge_su4.png]]