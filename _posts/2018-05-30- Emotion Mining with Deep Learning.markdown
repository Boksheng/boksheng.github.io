---
layout: post
---

![](/uploads/01.jpeg){: .fit.image}

## How are You Feeling Today?

Text is a difficult medium for communicating emotions. Is there a way to predict how a person is feeling based on what he or she writes?

This project is made to explore emotion mining using deep learning and it has 2 parts to it:

1. Emotion Mining on Text
2. Construction of Emotion Profile of a Novel

## Part 1: Emotion Mining on Text

#### Problem Statement:

To predict emotion (Anger, Joy, Sadness, Shame, Guilt and Disgust) from a given text

#### Technique:

Emotion Mining using Long Short Term Model (LSTM). Multi-class Text Classification problem

#### Baseline Model Comparison:

Support Vector Machine(SVC) and Multinomial Naive Bayes(MNB)

#### Data: The International Survey on Emotion Antecedents and Reactions (ISEAR)

A compilation of 7,666 sentences provided by 1,096 culturally divergent participants who were questioned about experiences and reactions that related to the emotions of anger, disgust, fear, joy, sadness, and guilt.

![](/uploads/isear-dataset-1.png)

#### Baseline Model Results (Accuracy)

The best result came from SVC with Count Vectorizer. 4 Variations:

1. SVC and Count Vectorizer
2. SVC and Tfidf
3. MNB and Count Vectorizer
4. MNB and Tfidf

#### Long Short Term Memory(LSTM)

The cell network takes three inputs.

1. X\_t is the input of the current time step.
2. h\_t-1 is the output from the previous LSTM unit
3. C\_t-1 is the “memory” of the previous unit
4. C\_t-1 goes through network and merge with X\_t to create new “memory” – C\_t.
5. h\_t is created from the network based
6. This single unit makes decision by considering the current input, previous ouput and previous memory

![](/uploads/lstm-2.png)

#### Building the LSTM

![](/uploads/lstm-build-2.png)

#### LSTM Results

![](/uploads/lstm-result-1.png)