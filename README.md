<p align="center">
  <img width="556" height="112" src="https://github.com/saksham189/GSOC-Work-Report/blob/master/src/logo.png">
</p>

#### Organisation: [mlpack](https://github.com/mlpack) 

#### Project: Implementing Essential Deep Learning Modules

#### Mentor: [Shikhar Jaiswal](https://github.com/ShikharJ)



## Overview
This summer I was selected as an intern for Google Summer of Code 2019 under mlpack. The following report summaries the work that was completed over 3 months as a part of my project “Implementing Essential Deep Learning Modules”.
mlpack is an open-source machine library in C++ built on top of the Armadillo library. The major goals of mlpack are scalability, speed and ease of use by implementing a consistent API for various machine learning algorithms. 

I started contributing to mlpack at the start of the year and have learnt a lot by contributing to it. My project this summer with mlpack was focused on generative adversarial networks that were first introduced by Ian Goodfellow.
The aim of my project was to add a set of improved training techniques for GANs since their training can be quite difficult in practice as well as support for Conditional GANs.

## Goal
In the past few years, research papers on GANs have grown exponentially and new GAN variants along with training methods are being discovered and published almost every week. There are [hundreds of GAN variants](https://github.com/hindupuravinash/the-gan-zoo) as of now.
The initial goal of my proposal for the project was to implement a few improved training techniques for GANs from this [paper](http://papers.nips.cc/paper/6124-improved-techniques-for-training-gans) as well as add support for [CGAN](https://arxiv.org/abs/1411.1784).
Namely we had decided to implement `Minibatch discrimination`, `Virtual batch normalization` and `One-sided label smoothing`.

## Results
We met most of the goals that I had proposed initially and were also able to work on adding additional training techniques. Most of the work is complete but requires testing after which it can be merged. 
In brief, the `VirtualBatch Normalisation layer` has been merged. The implementation of `MinibatchDiscrimination layer` is also complete. The implementation of conditional GAN is complete but needs to be tested.

[Virtual Batch Normalization](https://github.com/mlpack/mlpack/pull/1926) (merged)

[Minibatchdiscrimination Layer and Inception score](https://github.com/mlpack/mlpack/pull/1913) (open)

[CGAN](https://github.com/mlpack/mlpack/pull/1961) (open)


Some of the additional work that was completed during this time included a framework for regularisers such as the commonly used `L1` and `L2` regularisers. Along with this adding support for `orthogonal regulariser` that is effective for training GANs. Other than this I worked on adding a `Padding layer` that 
was useful to remove redundancy from various convolutional layers. Lastly, I have been working on `Spectral Normalization` technique for GANs which is still in progress.

[Regularizers and orthogonal regulariser for GANs](https://github.com/mlpack/mlpack/pull/1932) (merged) 

[Padding layer](https://github.com/mlpack/mlpack/pull/1952) (merged)

[SpectralNorm layer](https://github.com/mlpack/mlpack/pull/1983) (open)

<p align="left">
  <img width="366" height="191" src="https://github.com/saksham189/GSOC-Work-Report/blob/master/src/contributions.png">
</p>

## Conclusion
I would like to continue contributing to mlpack since I learnt a lot by contributing to the library and it aligns perfectly with my own interests. The area of generative adversarial networks is still relatively new and there are a lot of research papers being published with new techniques and variants. 
We hope to have support for these latest techniques in mlpack. Some of the interesting papers in the field that might be worth considering are:

[InfoGAN: Interpretable Representation Learning by Information Maximizing Generative Adversarial Nets](https://arxiv.org/abs/1606.03657)

[Conditional Image Synthesis With Auxiliary Classifier GANs](https://arxiv.org/abs/1610.09585)

I also hope to finish the testing of my currently open PR’s and have them merged. 


## Acknowledgments 
On a final note, I would like to thank my mentor Shikhar and Marcus for their timely reviews on all my PRs and patience when I was getting stuck. Without their help this project would have been nearly impossible to finish on time.  
I am also thankful to Ryan for his help when I initially started contributing to mlpack. mlpack was the first machine learning library that I contributed to and it helped me learn so much more about machine learning as well as writing efficient implementations of these algorithms in C++.  
I would also like to thank Google for sponsoring this program and giving us the opportunity to work on wonderful projects!

