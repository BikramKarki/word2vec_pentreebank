# word2vec_treebank
This code is an implementation of the Word2Vec algorithm. Specifically, it generates the word embeddings of a corpus by training a skip-gram model with negative sampling. The code downloads the Penn Treebank dataset, subsamples it, and uses it as the corpus. The code also defines a Vocab class for constructing the vocabulary and a RandomGenerator class for generating negative samples. Finally, the code defines functions for getting the centers and contexts of the corpus, and for getting the negative samples.

The download_extract function downloads a dataset from an URL, unzips it, and returns the path to the unzipped directory. The download function downloads a file from an URL and saves it in the specified folder. If the file already exists in the folder, it checks the SHA-1 hash of the file to ensure that the download is complete.

The corpus_read function reads the Penn Treebank dataset from a file and returns a list of sentences. The Vocab class constructs the vocabulary from the corpus, where tokens with a frequency less than a given threshold are ignored. The subsampling function subsamples the corpus using the subsampling technique described in the Word2Vec paper. The corpus_count function counts the frequency of each token in the corpus.

The get_centers_and_contexts function gets the centers and contexts of the corpus. For each sentence in the corpus, it generates pairs of (center, context), where the context is a list of tokens around the center token within a given window size. The RandomGenerator class generates negative samples using the unigram distribution raised to the power of 0.75, as described in the Word2Vec paper. The get_negatives function generates negative samples for a list of contexts using the RandomGenerator class.

corpus is from treebank-3 of Linguistic Data Consortium
