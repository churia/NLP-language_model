# Analysis of language models

### Comparison of the following models

- N-gram model 
- Neural Network language model (NNLM)
- Recurrent Neural Network language model (RNN)
- Skip-gram model and Word2vec

### Experiment
Since language model prefers sentences that are more frequently observed and grammatical, a reasonable way to evaluate a language model is to test whether it will pick real sentence out of some random generated sentence. So we evaluate the performances of the above language models by completing an open shared task for language modelling in _**lmtask**_: http://www.marekrei.com/teaching/lmtask

### Implement and Toolkit
- N-gram: We use SRILM toolkit (http://www.speech.sri.com/projects/srilm) to do the experiment. We've tried bigram, trigram and four-gram with Good Turing and Katz.
- NNLM: We use the java source code provided by _**lmtask**_, and implement the feedforward phase with sigmoid and softmax function and backprogration phase without regularization by our own. 
- RNNLM: We use RNNLM toolkit (http://www.fit.vutbr.cz/~imikolov/rnnlm) to do the experiment. We've tried different numbers of hiddens and classes and BPTTs.
- Skip-gram. We test word2vec toolkit from https://code.google.com/p/word2vec/.
