# SentenceEmbedding_InferSent - Sentence Embedding using InferSent

## Sentence Embedding Model - Infersent,
1) Load the file in Contect folder and use the model to perform Sentence embedding on the file",
2) This Model Uses some function models.py and extract_features.py which needs to be present in the same location as the code",
3) The Model does the encoding to generate the vectors. NOTE : The Word to Vectore packages for this Model needs to be in the Local machines / in content folder for the model to work well .\n",
"Example : W2V_PATH = 'content/GloVe/glove.840B.300d.txt' if model_version == 1 else 'content/fastText/crawl-300d-2M.vec'",
4) Uses the function cosine(u, v) to calculate the Cosine Similarity of the vectors

**Download the word vectors to the Model**
The First version is GloVe (V1) or fastText (V2) vectors: To download them the below funciton are used.

mkdir GloVe
curl -Lo GloVe/glove.840B.300d.zip http://nlp.stanford.edu/data/glove.840B.300d.zip
unzip GloVe/glove.840B.300d.zip -d GloVe/

mkdir fastText
curl -Lo fastText/crawl-300d-2M.vec.zip https://dl.fbaipublicfiles.com/fasttext/vectors-english/crawl-300d-2M.vec.zip
unzip fastText/crawl-300d-2M.vec.zip -d fastText/


**DOWNLOAD** THE models.py and extract_features.py files to the folder where the python code is present
To use this Model two functions has to be used where the code is present namely models.py and extract_features.py . The Implementaion is at  NLP_Part2_SentenceEmbedding_InferSent.ipynb . 

Get started with the following steps:

Download  InferSent models (V1 trained with GloVe, V2 trained with fastText)[147MB]:

**Note that infersent1 is trained with GloVe (which have been trained on text preprocessed with the PTB tokenizer) and infersent2 is trained with fastText (which have been trained on text preprocessed with the MOSES tokenizer). The latter also removes the padding of zeros with max-pooling which was inconvenient when embedding sentences outside of their batches.**
