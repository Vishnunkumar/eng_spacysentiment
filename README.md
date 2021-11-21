# spacysentiment
sentiment analysis using spacy

## Implementation

### Method - 1


- __Install the package using below command__

```
pip install eng-spacysentiment
```
- [PyPi](https://pypi.org/project/eng-spacysentiment/)

- __Implement the below code to get sentiment using spacy__

```python
import eng_spacysentiment
nlp = eng_spacysentiment.load()
text4 = "Welcome to Arsenal's official YouTube channel Watch as we take you closer and show you the personality of the club."
doc = nlp(text4)
doc.cats
```

- __Result__
```
input_text =  Its completely useless mate, we can do it the way we want
docs.cats = {'positive': 0.29878824949264526, 'negative': 0.7012117505073547}
```

- __Benchmarks__

The following metrics are generated from 300 randomly selected tagged sentences from [Emotion](https://www.kaggle.com/sankha1998/emotion) dataset, kindly take note that happy has been mapped as positive, while sad and angry has been mapped as negative.

| MODEL          | F1-score                           |
| -----          | ---------------------------------- |
| SpacySentiment | 0.65 |
| VaderSentiment | 0.68 |
| TextBlob       | 0.70                              |

### Method - 2

- __Clone the repository to your local__

```
cd spacysentiment/
unzip spacysentiment.zip
```

- __Implement the below code to get sentiment using spacy__

```python
import eng
nlp = spacy.load("spacysentiment")
input_text = input()
doc = nlp(input_text)
doc.cats
```

- __Result__
```
input_text =  Its completely useless mate, we can do it the way we want
docs.cats = {'positive': 0.29878824949264526, 'negative': 0.7012117505073547}
```


- [__Data Source__](https://archive.ics.uci.edu/ml/datasets/Sentiment+Labelled+Sentences) - UCI sentiment labelled sentences data, I used imbd part of data to train the model

- __Training__ : To train your own model please refer to [notebook](spacy-sentiment.ipynb)
