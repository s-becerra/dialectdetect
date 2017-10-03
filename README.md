## Readme
# Native Language classification

## Overview

Using audio samples from [The Speech Accent Archive](http://accent.gmu.edu/), I wanted to show that a deep neural network can classify the native language of a speaker.


## Table of Contents
1. [Dependencies](https://github.com/srbecerra/DialectDetect/blob/master/README.md#dependencies)
2. [Motivation](https://github.com/srbecerra/DialectDetect/blob/master/README.md#motivation)
3. [Data](https://github.com/srbecerra/DialectDetect/blob/master/README.md#data)
4. [Model](https://github.com/srbecerra/DialectDetect/blob/master/README.md#model)
5. [Running Model](https://github.com/srbecerra/DialectDetect/blob/master/README.md#running-model)
6. [Performance](https://github.com/srbecerra/DialectDetect/blob/master/README.md#performance)

## Dependencies
  * [Python 2.7](https://www.python.org/download/releases/2.7/)
  * [Keras](https://keras.io/)
  * [Numpy](http://www.numpy.org/)
  * [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/)
  * [Pydub](https://github.com/jiaaro/pydub)
  * [Sklearn](http://scikit-learn.org/stable/)
  * [Librosa](http://librosa.github.io/librosa/)

## Data
I started with the data from The Speech Accent Archive, a collection of 2447 audio samples from people for over 300 countries speaking the same English paragraph. The paragraph contains most of the consonants, vowels, and clusters of standard American English. It wasn’t useful to use the 9 audio samples from Finland.

For the purpose of this project, I focused on countries with the most abundant audio samples, and the languages that have distinctly different origins. I chose to work with English, Arabic, and Mandarin. After some filtering and to maintain a balanced dataset, I could only use 73 audio samples from each of the three languages.

## Model
Converted wav audio files into Mel Frequency Cepstral Coefficients graph. Fed into a 2D Convolutional Network to predict native language class.

## Challenges & Solutions
* Computationally expensive
* Small dataset

Created an Amazon Web Services Elastic Compute Cloud (EC2) instance that allowed for splitting workload over 32 cores.

MFCCs were sliced into smaller segments and randomly horizontally shifted after each epoch.

## Running Model
TODO

## Performance
|Act/Pred|English|Arabic|Mandarin|
|:-:|:-:|:-:|:-:|
|English|12|1|1|
|Arabic|5|8|1|
|Mandarin|1|1|14|
