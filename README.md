# Soraberta: Unsupervised Language Model Pre-training for Wolof

**Soraberta** is pretrained roberta-base model on wolof language  . Roberta was introduced in [this paper](https://arxiv.org/abs/1907.11692)

## Soraberta models

| Model name | Number of layers | Attention Heads | Embedding Dimension | Total Parameters |
| :------:       |   :---: | :---: | :---: | :---: |
| `soraberta-base` | 6    | 12   | 514   | 18 M |
 



## Using Soraberta with Hugging Face's Transformers


```python
>>> from transformers import pipeline
>>> unmasker = pipeline('fill-mask', model='abdouaziz/soraberta')
>>> unmasker("juroom naari jullit man nanoo boole jend aw nag walla <mask>.")

[{'sequence': 'juroom naari jullit man nanoo boole jend aw nag walla gileem.',
  'score': 0.9783930778503418,
  'token': 4621,
  'token_str': ' gileem'},
 {'sequence': 'juroom naari jullit man nanoo boole jend aw nag walla jend.',
  'score': 0.009271537885069847,
  'token': 2155,
  'token_str': ' jend'},
 {'sequence': 'juroom naari jullit man nanoo boole jend aw nag walla aw.',
  'score': 0.0027585660573095083,
  'token': 704,
  'token_str': ' aw'},
 {'sequence': 'juroom naari jullit man nanoo boole jend aw nag walla pel.',
  'score': 0.001120452769100666,
  'token': 1171,
  'token_str': ' pel'},
 {'sequence': 'juroom naari jullit man nanoo boole jend aw nag walla juum.',
  'score': 0.0005133090307936072,
  'token': 5820,
  'token_str': ' juum'}]
```

## Training data
The data sources are [Bible OT](http://biblewolof.com/) , [WOLOF-ONELINE](http://www.wolof-online.com/) 



## Contact

Please contact abdouaziz@gmail.com for any question, feedback or request.