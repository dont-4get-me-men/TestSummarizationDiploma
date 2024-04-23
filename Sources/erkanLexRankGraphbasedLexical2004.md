## LexRank: Graph-based Lexical Centrality as Salience in Text Summarization
Author: G. Erkan, D. R. Radev
year: 2004


### Notes

<mark class="customZot-Yellow ">Extractivesummarization works bychoosing asubset ofthe sentences inthe original documents. This process can beview ed asiden tifying the most central sentences ina(multidocument)cluster that givethe necessary and su cientamoun tofinformation related to the main theme ofthe cluster. Centralityofasen tence isoften de ned interms ofthe centralityofthe words that itcon tains. Acommon wayofassessing word centralityisto look atthe centroid ofthe documentcluster inavector space. The centroid ofacluster isapseudo-do cumentwhic hconsists ofwords that havetf  idf scores aboveaprede ned threshold, where tfisthe frequency ofaword inthe cluster, and idf values are typically computed overamuchlarger and similar genre data set.</mark> ([3](zotero://open-pdf/library/items/WG4YB8BF?page=3&annotation=THV9DLFF))

 
<mark class="customZot-Yellow ">The similaritybetween twosen tences isthen de ned bythe cosine between twocorresp onding vectors:</mark> ([4](zotero://open-pdf/library/items/WG4YB8BF?page=4&annotation=6WBFJUBE))

  
>using cosine similarity

<mark class="customZot-Yellow ">Astraigh tforward wayofform ulating this idea istoconsider every node having acen tralityvalue and distributing this centralitytoits neighbors. This formulation can beexpressed bythe equation p(u)= X v2adj[u] p(v) deg(v) (3) where p(u)isthe centralityofnode u, adj[u]isthe set ofnodes that are adjacentto u,and deg(v)isthe degree ofthe node v.Equiv alently,wecan write Equation 3inthe matrix notation as</mark> ([9](zotero://open-pdf/library/items/WG4YB8BF?page=9&annotation=PM3DL4RK))

   ![[power_method_lex_rank.png]]  ![[algoLexRank.png]]  ![[page_rank_with_idfcosine.png]]
<mark class="customZot-Yellow ">Graph-based centralityhas several advantages overCen troid. First ofall, itaccoun tsfor information subsumption among sentences. Ifthe information contentofasen tence subsumes another sentence inacluster, itisnaturally preferred toinclude the one that contains more information inthe summary.The degree ofanodeinthe cosine similaritygraph isan indication ofhowmuchcommon information the sentence has with other sentences. Sentence d4s1 inFigure 1gets the highest score since italmost subsumes the information inthe  rst twosen tences ofthe cluster and has some common information with others. Another advantage ofour proposed approachisthat itprev entsunnaturally high idf scores from boosting up the score ofasen tence that isunrelated tothe topic. Although the frequency ofthe words are taken intoaccoun twhile computing the Centroid score, asen tence that contains manyrare words with high idf values mayget ahigh Centroid score even ifthe words do not occur elsewhere inthe cluster.</mark> ([12](zotero://open-pdf/library/items/WG4YB8BF?page=12&annotation=VRV4TKRV))

  
>why use centrality

<mark class="customZot-Yellow ">This e ect ofthreshold isan indication that our new centralitymetho dsactually work for extractivesummarization. The higher the threshold, the less informative,oreven misleading, similaritygraphs wemust have.On the extreme pointwhere wehaveavery high threshold, wewould havenoedges inthe graph sothat Degree orLexRank centralitywould beofno use.</mark> ([14](zotero://open-pdf/library/items/WG4YB8BF?page=14&annotation=XC7563N7))

  
>proof that this is wokr
