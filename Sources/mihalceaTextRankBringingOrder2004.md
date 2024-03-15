Year: 2004
Authors: Rada Mihalcea, Paul Tarau


Title:: TextRank: Bringing Order into Text
URL: https://aclanthology.org/W04-3252
Zotero Link: [Full Text PDF](zotero://select/library/items/SU38TTDT)




> Itisimportant tonotice that although the TextRank applications described in this paper rely on an algorithm derived from Google’sPageRank (Brin and Page, 1998), other graph-based ranking algorithms such as e.g. HITS (Kleinberg, 1999) or Positional Function (Herings et al., 2001) can be easily integrated into the TextRank model (Mihalcea, 2004).
> 
> 



> 1. Identify text units that best define the task at hand, and add them as vertices in the graph. 
> 2. Identify relations that connect such text units, and use these relations to draw edges between vertices in the graph. Edges can be directed or undirected, weighted or unweighted. 
> 3. Iteratethegraph-basedrankingalgorithmuntilconvergence. 
> 4. Sortverticesbasedontheirfinalscore. Usethevaluesattachedtoeachvertexfor ranking/selectiondecisions.
> 
> 


> afrequenc ycriterion to select the “important” keywords in adocument.
> 
> 


> The state-ofthe-art in this area iscurrently represented by supervised learning methods, where asystem istrained to recognize keywords in atext, based on lexical and syntactic features
> 
> 


> where aNai veBayes learning scheme isapplied on the document collection, with improved results observed on the same data set as used in(Turne y,1999).
> 
> 


> the text is tokenized, and annotated with part of speech tags –apreprocessing step required to enable the application of syntactic filters. Toavoid excessivegro wth of the graph size by adding all possible combinations of sequences consisting of more than one lexical unit (ngrams), we consider only single words as candidates for addition to the graph, with multi-word keywords being eventually reconstructed in the post-processing phase. Next, all lexical units that pass the syntactic filter are added tothe graph, and an edge isadded between those lexical units that co-occur within awindo w of words. After the graph isconstructed (undirected unweighted graph), the score associated with each vertexisset to an initial value of 1, and the ranking algorithm described in section 2isrun on the graph for several iterations until itcon verges –usually for 20-30 iterations, atathreshold of 0.0001. Once afinal score isobtained for each vertexinthe graph, vertices are sorted in reversed order of their score, and the top vertices in the ranking are retained for post-processing. While may be set to anyfix ed value, usually ranging from 5to 20 keywords (e.g. (Turney,1999) limits the number of keywords extracted with his GenEx system to five), we are using amore flexible approach, which decide
> 
> 
> text Rank algo keyword



> the number of keywords based on the size of the text. For the data used in our experiments, which consists of relatively short abstracts, isset to athird of the number of vertices in the graph. During post-processing, all lexical units selected as potential keywords by the TextRank algorithm are marked in the text, and sequences of adjacent keywords are collapsed into amulti-w ord keyword. For instance, in the text Matlab code for plotting ambiguity functions,ifboth Matlab and code are selected as potential keywords by TextRank, since theyare adjacent, theyare collapsed into one single keyword Matlab code
> 
> 
> text Rank algo keyword



> Toapply TextRank, we first need to build agraph associated with the text, where the graph vertices are representativefor the units to be ranked. For the task of sentence extraction, the goal isto rank entire sentences, and therefore averte xisadded to the graph for each sentence in the text. The co-occurrence relation used for keyword extraction cannot be applied here, since the textunits in consideration are significantly larger than one or few words, and “co-occurrence” isnot ameaningful relation for such large contexts. Instead, we are defining adif ferent relation, which determines aconnection between twosentences ifthere is a“similarity” relation between them, where “similarity” ismeasured as afunction of their content overlap. Such arelation between twosentences can be seen as aprocess of “recommendation”: asentence that addresses certain concepts in atext, gives the reader a“recommendation” torefer to other sentences inthe text that address the same concepts, and therefore alink can be drawn between anytwosuch sentences that share common content. The overlap of twosentences can be determined simply as the number of common tokens between the lexical representations of the twosentences, or itcan be run through syntactic filters, which only count words of acertain syntactic category,e.g. all open class words, nouns and verbs, etc. Moreover, to avoid promoting long sentences, we are using a normalization factor,and divide the content overlap
> 
> 
> sentence extraction method



> of twosentences with the length of each sentence. Formally,given twosentences   and ,with a sentence being represented by the set of   words that appear in the sentence:          	       	       	      $ , the similarity of   and   isdefined as:   
	  
           K     	   2                    $           4    !#" $ %     $   & ' !#" $ %     4   & Other sentence similarity measures, such as string kernels, cosine similarity,longest common subsequence, etc. are also possible, and we are currently evaluating their impact on the summarization performance. The resulting graph is highly connected, with a weight associated with each edge, indicating the strength of the connections established between various sentence pairs in the text. The text istherefore represented as aweighted graph, and consequently we are using the weighted graph-based ranking formula introduced in Section 2.2. After the ranking algorithm is run on the graph, sentences are sorted in reversed order of their score, and the top ranked sentences are selected for inclusion in the summary. Figure 3sho ws atext sample, and the associated weighted graph constructed for this text. The figure also shows sample weights attached to the edges connected to vertex9 4,and the final TextRank score computed for each sentence. The sentences with the highest rank are selected for inclusion inthe abstract. For this sample article, the sentences with id-s 9,15, 16, 18 are extracted, resulting in asummary of about 100 words, which according to automatic evaluation measures, is ranked the second among summaries produced by 15 other systems (see Section 4.2 for evaluation methodology).
> 
> 
> text extraction method



> vely drawn from the entire text (graph). Through the graphs itbuilds on texts, TextRank identifies connections between various entities in a text, and implements the concept of recommendation. A text unit recommends other related text units, and the strength of the recommendation isrecursively computed based on the importance of the units making the recommendation.
> 
> 


> Through its iterativemechanism, TextRank goes beyond simple graph connectivity,and itis able to score text units based also on the “importance” of other textunits theylink to.
> 
> 


> An important aspect of TextRank is that itdoes not require deep linguistic knowledge, nor domain or language specific annotated corpora, which makes ithighly portable toother domains, genres, or languages.
> 
> 
> textRank benefits


