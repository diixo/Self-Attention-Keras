# IMDB text classification with Keras

This warehouse implements text classification based on the self-attention mechanism.

## Dependencies

- Python 3.5
- Keras 

## Dataset IMDB

IMDB movie review tendency classification data set, 25.000 movie reviews from IMDB, are marked as positive/negative reviews. Movie reviews have been preprocessed into sequences of word subscripts. For convenience, the subscript of a word is calibrated based on its frequency of occurrence in the dataset. For example, the word encoded by the integer 3 is the third most frequently occurring word in the dataset.

By convention, 0 does not represent any specific word, but is used to encode any unknown word.

## Usage

### Train
```bash
$ python imdb_attention.py
```

### Comparing results

|Algorithm|Training time (per epoch)|Validation accuracy|Validation loss|Number of Epochs required|
|---|---|---|---|---|
|LSTM|116s|0.8339|0.3815|2|
|Bidirectional LSTM|299s|0.8468|0.3475|1|
|CNN|9s|0.8916|0.2713|3|
|CNN LSTM|44s|0.8578|0.3435|2|
|Pretrained word vector (fasttext)|4s|0.8916|0.2763|7|
|Transformer|8s|0.8432|0.3500|2|

### Conclusion

The performance of the latest and most popular Transformer model (Transformer, that is, multi-head self-attention) on this classic small text classification data set is only moderate.

![image](https://github.com/foamliu/Self-Attention-Keras/raw/master/images/XunlianShijian.PNG)

![image](https://github.com/foamliu/Self-Attention-Keras/raw/master/images/Zhunquelv.PNG)




