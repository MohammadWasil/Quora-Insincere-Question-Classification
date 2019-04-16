# Quora-Insincere-Question-Classification

![quora](https://user-images.githubusercontent.com/31696557/56229984-da94ef80-6098-11e9-925c-242510267264.jpg)

Quora is a platform that empowers people to learn from each other. On Quora, people can ask questions and connect with others who contribute unique insights and quality answers.

This is a Kaggle Competition : [Quora Insincere Questions Classification.](https://www.kaggle.com/c/quora-insincere-questions-classification)

## Dependencies

You can install dependencies by running the following command in colab notebook:
'''
#To install pydrive
!pip install -U -q PyDrive
'''
To download Kaggle dataset directly to google colab disk:
1) Sign in to Kaggle.
2) Download kaggle json file.
3) In google colab, upload that file.
4) Then install the required packages:
'''
!pip install -q kaggle
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!ls ~/.kaggle
'''

Now, you can download the dataset:
'''
!kaggle competitions download -c quora-insincere-questions-classification
'''
To instakll requests package:
'''
!pip install requests
'''


## Dataset

