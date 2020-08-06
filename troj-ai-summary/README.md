# Extractive Text summarization

The Jupyter notebook *Extractive_Summarization_of_Scientific_Articles.ipynb*
extracts sentences from scientific articles text to serve as a summary of the
articles. The method is described within the notebook itself.

There are two versions of this notebook. The first is in the *master* branch and
contains no embedded outputs. This version allows for easier diffs of the code
and comments. The second is in the *master-output* and serves to document the
type of outputs to be expected.

The text can be obtained from article PDF files using *pdftotext*. We recommend
doing the following:

1. Create a *data* directory in directory containing the notebook with two subdirectories *pdf* and *text*.
2. Put the article PDF files in *data/pdf*.
3. Extract the article text from the PDF files into text files in *data/text* using:
```
pdftotext -raw pdf/article.pdf text/article.txt
```

The notebook should then be able to use the files in the *data/text* directory.
