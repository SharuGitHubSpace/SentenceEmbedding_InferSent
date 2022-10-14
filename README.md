# SentenceEmbedding_InferSent - Sentence Embedding using InferSent

This code is written in python. Dependencies include:

Python 2/3
Pytorch (recent version)
NLTK >= 3

**Download word vectors**
Download GloVe (V1) or fastText (V2) vectors:

mkdir GloVe

curl -Lo GloVe/glove.840B.300d.zip http://nlp.stanford.edu/data/glove.840B.300d.zip

unzip GloVe/glove.840B.300d.zip -d GloVe/

mkdir fastText

curl -Lo fastText/crawl-300d-2M.vec.zip https://dl.fbaipublicfiles.com/fasttext/vectors-english/crawl-300d-2M.vec.zip

unzip fastText/crawl-300d-2M.vec.zip -d fastText/




**Use our sentence encoder**
We provide a simple interface to encode English sentences. 
See NLP_Part2_SentenceEmbedding_InferSent.ipynb for implementation. 

Get started with the following steps:

 Download  InferSent models (V1 trained with GloVe, V2 trained with fastText)[147MB]:

mkdir encoder

curl -Lo encoder/infersent1.pkl https://dl.fbaipublicfiles.com/infersent/infersent1.pkl

curl -Lo encoder/infersent2.pkl https://dl.fbaipublicfiles.com/infersent/infersent2.pkl


**Note that infersent1 is trained with GloVe (which have been trained on text preprocessed with the PTB tokenizer) and infersent2 is trained with fastText (which have been trained on text preprocessed with the MOSES tokenizer). The latter also removes the padding of zeros with max-pooling which was inconvenient when embedding sentences outside of their batches.**

**DOWNLOAD** THE models.py and extract_features.py files to the folder where the python code is present
