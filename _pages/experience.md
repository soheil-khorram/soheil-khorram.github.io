---
permalink: /experience/
title: ""
excerpt: "Experience"
author_profile: true
layout: archive
---
<a name="top"></a>
# Experience
### Speech Enhancement/Separation
* GAN-based speech enhancement for CI users [ <span style="color:blue;"><a href="#gan-enhancement">read more</a></span> ]
* CNN-based speech enhancement in CI auditory space [ <span style="color:blue;"><a href="#cnn-enhancement">read more</a></span> ]
* Speech separation using probabilistic PIT [ <span style="color:blue;"><a href="#pit">read more</a></span> ]
### Emotion Recognition
* Recognizing continuous emotion labels using MDS network [ <span style="color:blue;"><a href="#mds-net">read more</a></span> ]
* Recognizing continuous emotion labels using large receptive field networks [ <span style="color:blue;"><a href="#lr-nets">read more</a></span> ]
* Progressive neural networks for transfer learning in computational paralinguistics [ <span style="color:blue;"><a href="#pnn">read more</a></span> ]
* Multimodal emotion recognition from speech and text [ <span style="color:blue;"><a href="#multimodal">read more</a></span> ]
### Mood Recognition
### Statistical Parametric Speech Synthesis
### Text-To-Speech

---

Speech Enhancement/Separation
-----------------------------

<a name="gan-enhancement"></a>
* ### GAN-based speech enhancement for CI users
An important question in developing DNN-based speech enhancement systems for CI users is, what optimization criterion should be used to train the networks? Mean square error (MSE) or log-MSE measures are normally used, but research in CI domain has shown that these measures do not correlate well with the speech intelligibility of CI users. Conditional generative adversarial network (CGAN) provides a solution by replacing the optimization loss functions with a discriminator network. In this project, I am exploring different methods of leveraging CGAN-based architectures to improve the speech intelligibility of CI users. [ <span style="color:green;"><a href="#top">back to top</a></span> ]

<a name="cnn-enhancement"></a>
* ### CNN-based speech enhancement in CI auditory space
To improve speech enhancement methods for CI users, I developed a set of convolutional neural network (CNN)-based speech enhancement systems in a cochlear filter-bank feature space, a feature-set specifically designed for CI users based on CI auditory stimuli. In this project, I tested three different CNN architectures: (1) vanilla CNN that directly generates the enhanced signal; (2) spectral-subtraction-style CNN (SS-CNN) that first predicts noise and then generates the enhanced signal by subtracting noise from the noisy signal; (3) Wiener-style CNN that generates an optimal mask for suppressing noise. Results showed that Wiener-style CNN provides a better speech enhancement system and It also outperforms the traditional speech enhancement systems.
[ [<span style="color:blue;">read more + code</span>](https://github.com/soheil-khorram/DNN-based-speech-enhancement) ]
[ <span style="color:green;"><a href="#top">back to top</a></span> ]

<a name="pit"></a>
* ### Speech separation using probabilistic PIT
Probabilistic permutation invariant training (Prob-PIT) improves and extends the conventional PIT for DNN-based speech separation systems. Prob-PIT considers the output-label permutation as a discrete latent random variable with a uniform prior distribution; all possible permutations have the same prior probability. It defines a log-likelihood function based on the prior distributions and the separation errors of all permutations. I showed that this structure can be easily implemented by replacing the minimum function of PIT with a soft-minimum function. Experimental results showed that Prob-PIT provides a smoother optimization landscape in the training phase of the separator network; therefore it can smooth out many local minima of the trining optimization landscape and lead to a better speech separator network.
[ [<span style="color:blue;">read more + code</span>](https://github.com/soheil-khorram/Prob-PIT) ]
[ <span style="color:green;"><a href="#top">back to top</a></span> ]

Emotion Recognition
-----------------------------

<a name="mds-net"></a>
* ### Recognizing continuous emotion labels using MDS network
Continuous emotion labels are generally not synchronized with the input speech signal due to delays caused by reaction-time, which is inherent in human evaluations. In order to train neural networks for continuous emotion recognition, a common method is to first compensate for the reaction-time delays by aligning continuous emotion labels with the speech signals. This approach assumes that the delay compensation and the emotion recognition are independent, yet they significantly depend on each other. To deal with this challenge, I introduced a new convolutional neural network, multi-delay sinc (MDS) network, that is able to simultaneously align and predict labels in an end-to-end manner. The proposed network is a stack of convolutional layers followed by an aligner network that aligns the speech signal and emotion labels. This network is implemented using a new convolutional layer that I introduced, the delayed sinc layer. It is a time-shifted low-pass (sinc) filter that uses a gradient-based algorithm to learn a single delay. I tested the efficacy of this system on two common emotion datasets, RECOLA (AVEC2016) and SEWA (AVEC2017), and showed that this approach obtains state-of-the-art speech-only results by learning time-varying delays while predicting dimensional descriptors of emotions.
[ [<span style="color:blue;">read more + code</span>](https://github.com/soheil-khorram/MDS-network) ]
[ <span style="color:green;"><a href="#top">back to top</a></span> ]

<a name="lr-nets"></a>
* ### Recognizing continuous emotion labels using large receptive field networks
In this project, I showed that capturing long-term temporal dependencies is critical for continuous emotion recognition tasks. To do so, I investigated two convolutional neural networks that are efficient in capturing large receptive fields: dilated networks and downsampling/upsampling networks. I showed that even though dilated networks outperform previously reported systems, the output signals produced from such architectures undergo erratic changes between consecutive time steps. This is inconsistent with the slow moving ground-truth emotion labels that are obtained from human annotators. Downsampling/upsampling network deals with this problem by modeling a downsampled version of the input signal and then generate the output signal through upsampling. Not only does the resulting downsampling/upsampling network achieve good performance, it also generates smooth output trajectories.
[ [<span style="color:blue;">read more</span>](capturing-long-term.pdf) ]
[ [<span style="color:blue;">code</span>](https://github.com/soheil-khorram/neural-network) ]
[ <span style="color:green;"><a href="#top">back to top</a></span> ]

<a name="pnn"></a>
* ### Progressive neural networks for transfer learning in computational paralinguistics
Many paralinguistic tasks are closely related and thus representations learned in one domain can be leveraged for another. In this project, I studied how knowledge can be transferred between three paralinguistic tasks: speaker, emotion, and gender recognition. Further, I extended this problem to cross-dataset tasks, asking how knowledge captured in one emotion dataset can be transferred to another. My main focus was on progressive neural networks and I compared these networks to the conventional deep learning methods of pre-training and fine-tuning. Experiments demonstrated that: (1) emotion recognition can benefit from using representations originally learned for different paralinguistic tasks and (2) transfer learning can effectively leverage additional datasets to improve the performance of emotion recognition systems.
[ [<span style="color:blue;">read more</span>](progressive.pdf) ]
[ <span style="color:green;"><a href="#top">back to top</a></span> ]

<a name="multimodal"></a>
* ### Multimodal emotion recognition from speech and text
In this project, I explored different ways of representing text and also different network architectures for combining text and speech representations. I used two common ways of representing text: (1) word2vec features and (2) a sequence of one-hot vectors that represent word's phonemes. I also tested different neural network architectures for combining two modalities including feature level fusion and intermediate level fusion techniques. For combining representations obtained from different modalities, I investigated various functions including summation, concatenation, multiplication and outer product functions.
[ [<span style="color:blue;">paper1</span>](exploiting_acoustic_and_lexical_properties.pdf) ]
[ [<span style="color:blue;">paper2</span>](pooling.pdf) ]
[ <span style="color:green;"><a href="#top">back to top</a></span> ]

Mood Recognition
----------------


Statistical Parametric Speech Synthesis
---------------------------------------


Text-To-Speech
---------------------------------------
