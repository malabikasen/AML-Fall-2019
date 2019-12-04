# AML-Fall-2019
Project repository/page for CS5824/ECE5424 - Advanced Machine Learning project. 

This page lists down the observations and results performed as a part of the project under **CS5824/ECE5424 Advanced Machine Learning** in Fall 2019 under *Prof. Dr. Bert Huang*. This project attempts to reproduce a finding from a Machine Learning Research study and present the results of the same.

## ABCNN: Attention-Based Convolutional Neural Network for Modelling Sentence Pairs
The [paper](https://arxiv.org/pdf/1512.05193.pdf) asserts that Attention-Based Convolutional Neural Networks (CNNs) perform better than CNNs without attention mechanisms. The paper integrated attention into CNNs for sentence pair modelling. Sentence pair modelling is a critical task in many Natural Language Processing (NLP) tasks such as Answer Selection, Paraphrase Identification and Textual Entailment. The experiments were performed for these three tasks. For this project, we are going to focus on Answer Selection.

## Background

Modeling a pair of sentences is a critical task for many NLP applications. 
<need to edit> 
s0 how much did Waterboy gross?
s1+ the movie earned $161.5 million
s1- this was Jerry Reed’s final film appearance
For AS, correctly answering s0 requires attention on “gross”: s1+ contains a corresponding unit (“earned”) while s1- does not.



## Setup

The experiments were run on a Windows Machine using Python with the following specifications -

1. Windows 10 Predator PH315-52/64-bit/i7/32GB RAM 
2. Python 3.7.4
3. tensorflow == 1.14.0
4. numpy == 1.17.4
5. sklearn == 0.21.3
5. [WikiQA Corpus](https://www.microsoft.com/en-us/download/details.aspx?id=52419)


## Experiment
The paper referred concludes that in Answer Selection the non-attention network BCNN already performs better than the baselines. Attention-based CNNs perform better than CNNs without attention mechanisms. For CNNs, they have test one (one-conv) and two (two-conv)
convolution-pooling blocks. The ABCNN-2 generally outperforms the  ABCNN-1 and the ABCNN3 surpasses both because, when combine the ABCNN-1 and the ABCNN-2 to form the ABCNN-3, as ability to take attention of finer-grained granularity into consideration in each convolution-pooling block. But, Due to the limited size of training data, increasing the number of convolutional layers did not show any significant improvement in the performance.
Baselines which thy have considered, the first three are by Yang et al. (2015): (i) WordCnt; (ii) WgtWordCnt; (iii) CNN-Cnt (the state-of-theart system): combine CNN with (i) and (ii). Apart from the baselines considered by Yang et al. (2015), they have also considered two LSTM baselines. Addition and A-LSTM 
In addition, linguistic features contribute in all three tasks: improvements by 0.0321 (MAP) and 0.0338 (MRR).
They concluded by stating Attention based models can be used to build really strong neural networks.





## Results

## Conclusion

## Papers



