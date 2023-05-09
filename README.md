# Sequence2Sequence-Machine-Translation

# Seq2Seq Machine Translation using TensorFlow 2.x

This repository contains an implementation of a sequence-to-sequence model for machine translation using TensorFlow 2.x. The model is trained on parallel corpora of English and French sentences and can translate French sentences to English.

## Data
The parallel corpora used in this project are directly accessible by using the datasets API. There are 233K train rows, 8.6K test rows and 890 validation rows
```
load_dataset('iwslt2017', 'iwslt2017-en-fr',cache_dir=dataset_path, verification_mode='no_checks')
```

## Dependencies
- Python 3.9
- TensorFlow 2.x
- TensorFlow Addons

To install the dependencies, run:
```
pip install -r requirements.txt
```

## Model Architecture
The model consists of an encoder and a decoder. The encoder is a 2-layer GRU network with an attention mechanism. The decoder is also a 2-layer GRU network with an attention mechanism. The input to the decoder at each timestep is a concatenation of the embedded input token and the context vector.

## Results
The model was trained on a parallel corpus of English and French sentences for 15 epochs. The final validation loss was 4.01. The model was able to translate English sentences to French with a BLEU score of 7.26.
