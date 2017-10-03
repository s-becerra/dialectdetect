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

## Running Model

## Performance
