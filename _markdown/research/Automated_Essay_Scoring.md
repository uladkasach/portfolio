# Automated Essay Scoring

This project is being conducted as part of my Research Assistantship under [Dr. Dundar][dundar_homepage], which started in fall of 2017.

This research began with the goal of attempting to evaluate several feature engineering hypotheses in utilizing word vectors to evaluate writing quality. A statistical exploratory data analysis was first conducted on the data and the hypothesized features. The features were then utilized in order to evaluate their ability to predict essay scores from the input text.

Hypotheses explored included utilizing word vectors to evaluate whether a word was being utilized in the right context or not through similarity, the affect that the parts of speech tree parsing had on word similarity, and more.

As of late November, I've been given authority to autonomously pursue a route of research in this domain which aligns closer to my interests, that is in representation learning. Most work in this field is dominated by feature engineering. Unsurprisingly, however, work has been done demonstrating that state of the art results can be acheived with representation learning. The future direction of this project will involve evaluating gaps left in the literature: for example how much of the information captured by hand-crafted features is captured by the representation and how will the model respond to transfer learning in the form of pretrained word embeddings, rather than custom trained?

For this research the [ASAP-AES Kaggle Dataset][dataset] is being used.

## Notable Findings

An interesting finding was that noun-adj pairs were consistently less similar (as captured by word embeddings) than verb-adj pairs:

![research_gif][parse_tree]


## Interesting Figures

TSNE applied to vector representations of essays generated by feature engineering which included parse tree similarity metrics generated in figures which were notably different from the rest of the vector representations that were created. The following diagrams demonstrate the average TSNE response and the response of TSNE on vectors created with the parse tree syntactic features respectivly:

![research_gif][regular_tsne]
![research_gif][synt_tsne]



[dundar_homepage]: https://cs.iupui.edu/~dundar/index.htm
[dataset]: https://www.kaggle.com/c/asap-aes


[parse_tree]:  /_material/research/Automated_Essay_Scoring/parse_tree.png
[regular_tsne]: /_material/research/Automated_Essay_Scoring/reg_tsne.png
[synt_tsne]: /_material/research/Automated_Essay_Scoring/pattern.png
