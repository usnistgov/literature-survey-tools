# Extractive Text summarization

The Jupyter notebook *Extractive_Summarization_of_Scientific_Articles.ipynb*
extracts sentences from scientific articles text to serve as a summary of the
articles. The method is described within the notebook itself.

The text can be obtained from article PDF files using *pdftotext*. We recommend doing the following:

1. Create a *data* directory in directory containing the notebook with two subdirectories *pdf* and *text*.
2. Put the article PDF files in *data/pdf*.
3. Extract the article text from the PDF files into text files in *data/text* using:
```
pdftotext -raw pdf/article.pdf text/article.txt
```

The notebook should then be able to use the files in the *data/text* directory.
