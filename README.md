
# Word Similarity Datasets for Thai Language

## Summary

This repo contains translated and re-rated datasets for **word similarity for Thai language**.
The four datasets are listed in the table below. The *Dataset* files are csv files, and just contain
the word pairs, and the similarity score between the two words.
Furthermore, we provide the individual annotator ratings as well as statistics (inter-annotator agreement,
correlation between TH and EN versions, etc.) in the *Dataset Details* files.   



|Name            | Dataset  | Number of word pairs   | Dataset Details |
|----------------| ------------- | -------------- | ------------- |
|TH-WordSim-353  | [th-wordsim-353.csv](th-wordsim-353.csv)  | 353  | [th-wordsim-353.details.xlsx](th-wordsim-353.details.xlsx)|
|TH-SimLex-999   | [th-simlex-999.csv](th-simlex-999.csv)    | 999  | [th-simlex-999-details.xlsx](th-simlex-999-details.xlsx)  |
|TH-SemEval-500  | [th-semeval-500.csv](th-semeval-500.csv)  | 500  | [th-semeval-500-details.xlsx](th-semeval-500-details.xlsx)|  
|TWS-65          | [tws65.csv](tws65.csv)                    | 65   | [tws65_full.csv](tws65_full.csv)                          |  

The datasets were created by KMITL University, Ladkrabang, Thailand (Dr. Ponrudee Netisopakul) together with ITMO University, St. Petersburg, Russia (Dr. Gerhard Wohlgenannt,
Aleksei Pulich). If you just seek for a way to easily evaluate your Thai models with these datasets, see: [https://github.com/gwohlgen/word-embeddings-benchmarks](https://github.com/gwohlgen/word-embeddings-benchmarks).

## The Datasets
* *TH-WordSim-353*: in based on [WordSim-353](http://www.cs.technion.ac.il/~gabr/resources/data/wordsim353/).
    The English WordSim-353 is the most popular word similarity dataset. It contains 353 word pairs, and measures the semantic relatedness and a scale from 0 to 10. 
    We translated the dataset to Thai, and rated the word pairs with 13 annotators. 

* *TH-SimLex-999*: in based on [SimLex-999](https://fh295.github.io/simlex.html).
    SimLex-999 is specifically designed to capture similarity between terms, as opposed to relatedness (like in WordSim-353).
    The dataset contains 666 noun, 222 verb and 111 adjective pairs. 
    Characteristics of this dataset are that it only includes words from the vocabulary of WordNet, 
    and that it contains a large number of antonymy pairs. In the English version, the similarity ratings were created with crowdsourcing via Amazon Mechanical Turk, 
    originally on a scale from 0 to 6, later linearly re-scaled to [0,10]. 
    *We translated the dataset to Thai and rated with 16 Thai native speakers as annotators.*

* *TH-SemEval-500*: in based on the dataset from [SemEval2017 (Task 2)](http://alt.qcri.org/semeval2017/task2/).
    SemEval-500 is a multilingual dataset for English, Farsi, German, Italian and Spanish for SemEval-2017, task 2.
    The dataset contains 500 word pairs. The goal is to provide a challenging dataset, which includes word pairs from 34 domains such as chemistry and mineralogy, computing, culture and society.
    Furthermore, the dataset contains named entities (e.g., Microsoft), or multiword expressions (e.g., black hole) in any of the 34 domains.
    For rating they use a 5-point Likert scale with a step size of 0.25, and the instructions for the annotators contain both the notions of relatedness and similarity, 
    in which similarity is rated higher.
    *We translated the dataset to Thai and rated with 16 Thai native speakers as annotators.*  

* *tws-65*: This dataset is found in [Osathanunkul et al.](https://link.springer.com/chapter/10.1007/978-3-642-22000-5_56). 
    This is work by Osathanunkul et al., we only loaded it into a .csv file and provide it here. 
    We provide 2 versions, one with only 3 columns (the Thai word pair and the rating), 
    and a version which includes the English terms and the stddev.

## Usage
We made a repository which you can use to very simply evaluate any Thai word embedding model, it is available here:
[https://github.com/gwohlgen/word-embeddings-benchmarks](https://github.com/gwohlgen/word-embeddings-benchmarks).




## Cite

Please cite our paper in *IEEE Access*: 
    `Ponrudee Netisopakul￼, Gerhard Wohlgenannt, Aleksei Pulich: Word Similarity Datasets for Thai: Construction and Evaluation. IEEE Access 7: 142907-142915 (2019)`

The paper is found here: [https://doi.org/10.1109/ACCESS.2019.2944151](https://doi.org/10.1109/ACCESS.2019.2944151)
>    @article{NetisopakulWP19,
>      author    = {Ponrudee Netisopakul and Gerhard Wohlgenannt and Aleksei Pulich},
>      title     = {Word Similarity Datasets for Thai: Construction and Evaluation},
>      journal   = {{IEEE} Access},
>      volume    = {7},
>      pages     = {142907--142915},
>      year      = {2019},
>      url       = {https://doi.org/10.1109/ACCESS.2019.2944151},
>      doi       = {10.1109/ACCESS.2019.2944151},
>    }


##  References
> *WordSim-353:* L. Finkelstein, E. Gabrilovich, Y. Matias, E. Rivlin, Z. Solan, G. Wolfman, and E. Ruppin, “Placing search in context: The concept revisited,” ACM Transactions on information systems, vol. 20, no. 1, pp. 116–131, 2002.

> *SimLex-999:* F. Hill, R. Reichart, and A. Korhonen, “Simlex-999: Evaluating semantic models with (genuine) similarity estimation,” Computational Linguistics, vol. 41, no. 4, pp. 665–695, 2015.
    [pdf on arxiv](https://arxiv.org/abs/1408.3456v1)

> *SemEval-500:* J. Camacho-Collados, M. T. Pilehvar, N. Collier, and R. Navigli, “Semeval-2017 task 2: Multilingual and cross-lingual semantic word similarity,” in Proc. 11th Int. Workshop on Semantic Evaluation (SemEval2017). Association for Computational Linguistics, 2017, pp. 15–26.

