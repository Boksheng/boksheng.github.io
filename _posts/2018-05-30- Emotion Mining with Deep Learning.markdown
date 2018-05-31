---
layout: post
---

![](/uploads/01.jpeg){: .fit.image}

## How are You Feeling Today?

Text is a difficult medium for communicating emotions. Is there a way to predict how a person is feeling based on what he or she writes?

This project is made to explore emotion mining using deep learning and it has 2 parts to it:

* Emotion Mining on Text
* Construction of Emotion Profile of a Novel

## Part 1: Emotion Mining on Text

&nbsp;

#### Problem Statement:

To predict emotion (Anger, Joy, Sadness, Shame, Guilt and Disgust) from a given text

#### Technique:

Emotion Mining using Long Short Term Model (LSTM). Multi-class Text Classification problem

#### Baseline Model Comparison:

Support Vector Machine(SVC) and Multinomial Naive Bayes(MNB)

#### Data: The International Survey on Emotion Antecedents and Reactions (ISEAR)

A compilation of 7,666 sentences provided by 1,096 culturally divergent participants who were questioned about experiences and reactions that related to the emotions of anger, disgust, fear, joy, sadness, and guilt.

![](/uploads/screen-shot-2018-05-31-at-10-19-16-2.png)

#### Baseline Model Results (Accuracy)

The best result came from SVC with Count Vectorizer. 4 Variations:

* SVC and Count Vectorizer
* SVC and Tfidf
* MNB and Count Vectorizer
* MNB and Tfidf

#### Long Short Term Memory(LSTM)

The cell network takes three inputs.

1. X\_t is the input of the current time step.
2. h\_t-1 is the output from the previous LSTM unit
3. C\_t-1 is the “memory” of the previous unit
4. C\_t-1 goes through network and merge with X\_t to create new “memory” – C\_t.
5. h\_t is created from the network based
6. This single unit makes decision by considering the current input, previous ouput and previous memory

![](/uploads/screen-shot-2018-05-31-at-10-20-46-3.png)

#### Building the LSTM

![](/uploads/screen-shot-2018-05-31-at-10-25-24-5.png)

#### LSTM Results

![](/uploads/screen-shot-2018-05-31-at-10-57-59-2.png)