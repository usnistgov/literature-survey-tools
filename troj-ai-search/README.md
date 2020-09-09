# Embedding-based Search for Scientific Abstracts

The Jupyter notebook Embedding_Based_Search_for_Scientific_Abstracts.ipynb contains a prototype embedding-based text search method that
uses an [flair](https://github.com/flairNLP/flair) embeddings and a [gensim](https://radimrehurek.com/gensim/) similarity index created from the computer science subset of [arXiv](https://arxiv.org/). It produces a list of the top-ranked abstracts as the results of the query. The method is described within the notebook itself.

There are two versions of this notebook. The first is in the master branch and contains no embedded outputs. This version allows for easier diffs of the code and comments. The second is in the master-output and serves to document the type of outputs to be expected.

## Installation

We are currently using older version of pytorch and flair as well as Python 3.7. The code will have to be updated to work with the latest versions.

The necessary packages can be installed as follows:

1. `conda install pytorch==1.3.0 torchvision==0.4.1 cudatoolkit=10.1 -c pytorch`
2. `pip install flair==0.4.3`
3. `pip install wordcloud`

The three steps above have been encapsulated in a Jupyter notebook, Setup.ipynb, which can be run to ensure a properly configured environment.

Binary files containing data generated from arXiv will also need to be present. These include:
* title-abstracts.idx
* title-abstracts.pkl
* index/title-abstracts.*
* language_model/arXiv-cs-lc-backward.pt
* language_model/arXiv-cs-lc-forward.pt

These files are available via the GitHub release mechanism (v0.1). Find them on this project's [release page](https://github.com/usnistgov/literature-survey-tools/releases). Download and unarchive them in the same directory as the notebook.

## Usage

Once the prerequisites are installed, the notebook can be run by first replacing the `qry` variable's value with that of a document's title and abstract for which similar documents are to be found and then rerunning the notebook. The `num_selected` variable sets the maximum number of ranked results returned.
