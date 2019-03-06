# SHAN (Not completed yet)


Keras implementation of [Syntax-Directed Hybrid Attention Network for Aspect-Level Sentiment Analysis](https://ieeexplore.ieee.org/document/8561296)

## Prerequisites
1. keras
2. spacy (pip install -U spacy)
3. pyenchant （pip install pyenchant）
4. python 2.7
5. nltk (pip install nltk)
6. download pretrained glove [glove.840B.300d.zip](https://nlp.stanford.edu/data/wordvecs/glove.840B.300d.zip) and unzip it in dir *GLOVE_MODEL*

## Preprocess
1. GetData.py : extract data from xml file
2. Pre.py :
    <!-- - transform sentence to low case 
    - Spell check 
    - filter stop words  
    - Lemmatization -->
    - cut sentence
    - transform label to one-hot vector
3. InputLayer.py : transform sentences and targets to glove vector format
4. LSK.py : Dependency parsing

After run step 1,2,3,4,we got:

dir *train*:
- train_label.npy (generated by Pre.py)
- train_target.npy (generated by Pre.py)
- train_x.npy (generated by Pre.py)
- glove_target_vec.npy(generated by InputLayer.py)
- glove_vec.npy(generated by InputLayer.py)
- LSK.npy(generated by LSK.py)


dir *test*:
- test_label.npy (generated by Pre.py)
- test_target.npy (generated by Pre.py)
- test_x.npy (generated by Pre.py)
- glove_target_vec.npy (generated by InputLayer.py)
- glove_vec.npy (generated by InputLayer.py)
- LSK.npy (generated by LSK.py)


## Usage
For training, `python Main.py train`
<br>
For testing, `python main.py test`

## Result

### train data
set validation_split=0.2
- 80% data training
- 20% data validating

categorical_accuracy:  
<br>
val_categorical_accuracy: 

### test data
accuracy: 

## Pretrained model
[no pretrained model](wwww.github.com)


## References
[Syntax-Directed Hybrid Attention Network for Aspect-Level Sentiment Analysis](https://ieeexplore.ieee.org/document/8561296)

