<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>

  <meta itemprop="name" content="natural_questions" />
  <meta itemprop="description" content="&#10;The NQ corpus contains questions from real users, and it requires QA systems to&#10;read and comprehend an entire Wikipedia article that may or may not contain the&#10;answer to the question. The inclusion of real user questions, and the&#10;requirement that solutions should read an entire page to find the answer, cause&#10;NQ to be a more realistic and challenging task than prior QA datasets.&#10;&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;natural_questions&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/natural_questions" />
  <meta itemprop="sameAs" content="https://ai.google.com/research/NaturalQuestions/dataset" />
  <meta itemprop="citation" content="&#10;@article{47761,&#10;title = {Natural Questions: a Benchmark for Question Answering Research},&#10;author  = {Tom Kwiatkowski and Jennimaria Palomaki and Olivia Redfield and Michael Collins and Ankur Parikh and Chris Alberti and Danielle Epstein and Illia Polosukhin and Matthew Kelcey and Jacob Devlin and Kenton Lee and Kristina N. Toutanova and Llion Jones and Ming-Wei Chang and Andrew Dai and Jakob Uszkoreit and Quoc Le and Slav Petrov},&#10;year   = {2019},&#10;journal   = {Transactions of the Association of Computational Linguistics}&#10;}&#10;" />
</div>

# `natural_questions`

The NQ corpus contains questions from real users, and it requires QA systems to
read and comprehend an entire Wikipedia article that may or may not contain the
answer to the question. The inclusion of real user questions, and the
requirement that solutions should read an entire page to find the answer, cause
NQ to be a more realistic and challenging task than prior QA datasets.

*   URL:
    [https://ai.google.com/research/NaturalQuestions/dataset](https://ai.google.com/research/NaturalQuestions/dataset)
*   `DatasetBuilder`:
    [`tfds.text.natural_questions.NaturalQuestions`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/text/natural_questions.py)
*   Version: `v0.0.2`
*   Versions:

    *   **`0.0.2`** (default):
    *   `0.0.1`: None

*   Download size: `Unknown size`

*   Dataset size: `90.26 GiB`

## Features
```python
FeaturesDict({
    'annotations': Sequence({
        'id': Tensor(shape=(), dtype=tf.string),
        'long_answer': FeaturesDict({
            'end_byte': Tensor(shape=(), dtype=tf.int64),
            'end_token': Tensor(shape=(), dtype=tf.int64),
            'start_byte': Tensor(shape=(), dtype=tf.int64),
            'start_token': Tensor(shape=(), dtype=tf.int64),
        }),
        'short_answers': Sequence({
            'end_byte': Tensor(shape=(), dtype=tf.int64),
            'end_token': Tensor(shape=(), dtype=tf.int64),
            'start_byte': Tensor(shape=(), dtype=tf.int64),
            'start_token': Tensor(shape=(), dtype=tf.int64),
            'text': Text(shape=(), dtype=tf.string),
        }),
        'yes_no_answer': ClassLabel(shape=(), dtype=tf.int64, num_classes=2),
    }),
    'document': FeaturesDict({
        'html': Text(shape=(), dtype=tf.string),
        'title': Text(shape=(), dtype=tf.string),
        'tokens': Sequence({
            'is_html': Tensor(shape=(), dtype=tf.bool),
            'token': Text(shape=(), dtype=tf.string),
        }),
        'url': Text(shape=(), dtype=tf.string),
    }),
    'id': Tensor(shape=(), dtype=tf.string),
    'question': FeaturesDict({
        'text': Text(shape=(), dtype=tf.string),
        'tokens': Sequence(Tensor(shape=(), dtype=tf.string)),
    }),
})
```

## Statistics

Split      | Examples
:--------- | -------:
ALL        | 315,203
TRAIN      | 307,373
VALIDATION | 7,830

## Homepage

*   [https://ai.google.com/research/NaturalQuestions/dataset](https://ai.google.com/research/NaturalQuestions/dataset)

## Citation

```
@article{47761,
title   = {Natural Questions: a Benchmark for Question Answering Research},
author  = {Tom Kwiatkowski and Jennimaria Palomaki and Olivia Redfield and Michael Collins and Ankur Parikh and Chris Alberti and Danielle Epstein and Illia Polosukhin and Matthew Kelcey and Jacob Devlin and Kenton Lee and Kristina N. Toutanova and Llion Jones and Ming-Wei Chang and Andrew Dai and Jakob Uszkoreit and Quoc Le and Slav Petrov},
year    = {2019},
journal = {Transactions of the Association of Computational Linguistics}
}
```

--------------------------------------------------------------------------------
