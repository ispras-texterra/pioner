# pioNER - named entity annotated datasets and GloVe models for the Armenian language

pioNER corpus provides gold-standard and automatically generated named-entity datasets for the Armenian language.

Alongside the datasets, we release 50-, 100-, 200-, and 300-dimensional GloVe word embeddings trained on a collection of Armenian texts from Wikipedia, news, blogs, and encyclopedia.

**Silver-standard dataset**

The generated corpus is automatically extracted and annotated using Armenian Wikipedia. We used a modification of [Nothman et al](https://www.researchgate.net/publication/256660013_Learning_multilingual_named_entity_recognition_from_Wikipedia) and [Sysoev and Andrianov](http://www.dialog-21.ru/media/3433/sysoevaaandrianovia.pdf) approaches to create this corpus. This approach uses links between Wikipedia articles to extract fragments of named-entity annotated texts.

The corpus is split into train and development sets. 

*Table 1. Statistics for pioNER train, development and test sets*

| dataset       | #tokens | #sents | annotation | texts' source |
|-------------|:--------:|:-----:|:--------:|:-----:|
| train    | 130719 |  5964  | automatic | Wikipedia |
| dev | 32528 | 1491 | automatic | Wikipedia |
| test | 53606 | 2529 | manual | iLur.am |

**Gold-standard dataset**

This dataset is a collection of over 250 news articles from iLur.am with manual named-entity annotation. It includes sentences from political, sports, local and world news, and is comparable in size with the test sets of other languages (Table 2). 
We aim it to serve as a benchmark for future named entity recognition systems designed for the Armenian language.

The dataset contains annotations for 3 popular named entity classes: 
people (PER), organizations (ORG), and locations (LOC), and is released in CoNLL03 format with IOB tagging scheme. 
During annotation, we generally relied on categories and [guidelines assembled by BBN](https://catalog.ldc.upenn.edu/docs/LDC2005T33/BBN-Types-Subtypes.html) Technologies for TREC 2002 question answering track

Tokens and sentences were segmented according to the UD standards for the Armenian language from [ArmTreebank project](http://armtreebank.yerevann.com/tokenization/process/).

*Table 2. Comparison of pioNER gold-standard test set with test sets for English, Russian, Spanish and German*

| test dataset       | #tokens | #LOC | #ORG | #PER |
|-------------|:--------:|:-----:|:--------:|:-----:|
| Armenian pioNER    | 53606 |  1312  | 1338 | 1274 |
| Russian factRuEval-2016 | 59382 | 1239 | 1595 | 1353 |
| German CoNLL03 | 51943 | 1035 | 773 | 1195 |
| Spanish CoNLL02 | 51533 | 1084 | 1400 | 735 |
| English CoNLL03 | 46453 | 1668 | 1661 | 1671 |

**GloVe embeddings**

We also publish GloVe word vector models trained on Armenian texts containing 79 million tokens.
The training set included the articles of Armenian Wikipedia, The Armenian Soviet Encyclopedia, a subcorpus of [Eastern Armenian National Corpus](http://eanc.net/), and news articles from over a dozen Armenian news websites and blogs. Texts covered topics such as economics, politics, weather forecast, IT, law, society and politics, coming from non-fiction as well as fiction genres.

Similar to the original embeddings published for the English language, we release 50-, 100-, 200- and 300-dimensional word vectors for Armenian with a vocabulary size of 400000.

You can download GloVe models from [here](https://at.ispras.ru/owncloud/index.php/s/eXNpONfB09TBpgI).

For more details, refer to the [paper](https://arxiv.org/pdf/1810.08699.pdf).


