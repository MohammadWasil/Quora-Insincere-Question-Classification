# Quora-Insincere-Question-Classification

![quora](https://user-images.githubusercontent.com/31696557/56229984-da94ef80-6098-11e9-925c-242510267264.jpg)

Quora is a platform that empowers people to learn from each other. On Quora, people can ask questions and connect with others who contribute unique insights and quality answers.

This is a Kaggle Competition : [Quora Insincere Questions Classification.](https://www.kaggle.com/c/quora-insincere-questions-classification). We will be predicting whether a question asked on Quora is sincere or not. An insincere question is defined as a question intended to make a statement rather than look for helpful answers. 

## Dependencies

You can install dependencies by running the following command in colab notebook:<Br/>
```
#To install pydrive
!pip install -U -q PyDrive
```
To download Kaggle dataset directly to google colab disk:
1) Sign in to Kaggle.
2) Download kaggle json file.
3) In google colab, upload that file.
4) Then install the required packages:<Br/>
```
!pip install -q kaggle
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!ls ~/.kaggle
```

Now, you can download the dataset:<Br/>
```
!kaggle competitions download -c quora-insincere-questions-classification
```

To install requests package:<Br/>
```
!pip install requests
```

## Dataset

There are Two datasets - 1) train data 2) Test data.

Train Data has 1.3m rows, with 3 columns - qid, question_text, target.<Br/>
Test data has 376k rows with only 2 columns - qid, and question_text. 

## Sentiment Analysis

Sentiment Analyses of the questions have been done using different Recurrent Neural Network(RNN) units like, Gated Recurrent Units(GRU),  and Long Short-term Memory(LSTM), and Convolutional Neural Network. We trained the model using different hyper-parameters(like, number of convolutional and dense layers, filter sizes, threshold value) to find the model with highest F1 score, since it is a skewed data.

|S.NO| RNN Unit | Convolutional block | Filter size | #Dense Layer | Threshold | Public Dataset | Private Dataset|
|----|----------|---------------------|-------------|--------------|-----------|----------------|----------------|
|  1 | LSTM     | 1                   | 64          | 1            | 0.299999  | 0.61660        | 0.61996        |
|  2 | GRU      | 1                   | 128         | 1            | 0.299999  | 0.63823        | 0.64841        |











