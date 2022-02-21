# Radio signals classifier

Classifier of over-the-air recordings of 24 digital and analog modulation of radio signals based on deep learning [ResNet architecture](https://en.wikipedia.org/wiki/Residual_neural_network).

## Dataset

A dataset that includes both synthetic simulated channel effects and over-the-air recordings of 24 digital and analog modulation types has been heavily validated.

This dataset was used for Over-the-air deep learning-based radio signal classification published 2017 in IEEE Journal of Selected Topics in Signal Processing, which provides additional details and a description of the dataset.

Data was stored in hdf5 format as complex floating-point values, with 2 million examples, each 1024 samples long. I converted the data to .npy format since I found it took much less time to load. You can find that below: [Link](https://www.kaggle.com/aleksandrdubrovin/deepsigio-radioml-201801a-new)

## Description

I conduct an in depth study on the performance of  deep learning based radio signal classification for radio communications signal.

## Approach

I was working with one third part of dataset (851968 signals), I found myself running into problems with memory shortages on Kaggle’s default and decided to use powerful Google Cloud Platform virtual machine instance. I used the virtual machine instance n1-standard-8 (8 vCPU, 30 GB memory) with a NVIDIA Tesla V100 GPU to run my training session.
This required about 7.5 hours of training time

## Conclusion 

The model achieved maximum accuracy of 95.72% on the clean signal dataset: [Signal-to-noise ratio](https://en.wikipedia.org/wiki/Signal-to-noise_ratio#:~:text=Signal-to-noise%20ratio%20(,power%2C%20often%20expressed%20in%20decibels.)) > 8 dB.

*Note that the maximum classification accuracy of 62% if you want to test the model to its absolute limits on a mix of clean signals and signals with very high interference. Some of the signals have so much noise that they are virtually unrecognizable.*

## Acknowledgements

Thanks to Tim O’Shea, Tamoghna Roy, T. Charles Clancy for posting [Over the Air Deep Learning Based Signal Classification](https://arxiv.org/pdf/1712.04578.pdf).
