# Self introduction generator with LSTM
A experimental model to generate self introduction with LSTM

## About
This dataset is scraped from various host/superhost from airbnb. 

## Aim
To assist airbnb user to generate self-introduction with deep learning model.

## Process
```
1. preprocess data before training.
2. Experiment 3 LSTM with various hyperparameters.
  1. Running the existing lstm model with 100 epochs. (Baseline model)
  2. Increase the number of training epochs to be 200 with layer 150.
  3. Add dropout to the visible input layer and consider tuning the dropout percentages.
3. Measure the performance /loss function.
```

## First and Second Pre-processing
```
1. Preprocessing
The initial preprocessing has already undergone before saving into scraping-test.csv. Initial preprocessing can be found in initial_preprocessing.py.
  Initial preprocessing does the follows:

  1. Replace contractions (i.e. from "isn't" to "is not", from "aren't" to "are not" and etc). More contractions examplescan be found in contractions.py
  2. Sets all text tower case
  3. Remove url links, including the url with starts with www. and/or https://www.
  4. Replaces all & to "and", to reduce texts ambiguity.
  5. Removes punctuation (i.e. !,.":@~! and etc.)
  6. Replaces all instances of the integer to string (i.e. from "2" to "two" and etc.)

2. Second preprocessing.
The second preprocessing in this jupyter will undergo several procedures before building the model.
The second preprocessing does the follows:
  1. Remove square brackets from the dataset.
  2. Splits the words up, then assigns a unique integer to each word
  3. Replaces all instances of that word with the integer.

```

## How to run ipynb file

```bash
pip install -r requirement.txt
jupyter lab 
```

