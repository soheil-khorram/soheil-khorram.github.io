---
permalink: /experience/
title: "Experience"
excerpt: "Experience"
author_profile: true
layout: archive
---

Speech Enhancement/Separation
-----------------------------

* ### GAN-based speech enhancement for CI users
An important question in developing DNN-based speech enhancement systems for CI users is, what optimization criterion should be used to train the networks? Mean square error (MSE) or log-MSE measures are normally used, but research in CI domain has shown that these measures do not correlate well with the speech intelligibility of CI users. Conditional generative adversarial network (CGAN) provides a solution by replacing the optimization loss functions with a discriminator network. In this project, I am exploring different methods of leveraging CGAN-based architectures to improve the speech intelligibility of CI users.

* ### CNN-based speech enhancement in CI auditory space
To improve speech enhancement methods for CI users, I developed a set of convolutional neural network (CNN)-based speech enhancement systems in a cochlear filter-bank feature space, a feature-set specifically designed for CI users based on CI auditory stimuli. In this project, I tested three different CNN architectures: (1) vanilla CNN that directly generates the enhanced signal; (2) spectral-subtraction-style CNN (SS-CNN) that first predicts noise and then generates the enhanced signal by subtracting noise from the noisy signal; (3) Wiener-style CNN that generates an optimal mask for suppressing noise. Results showed that Wiener-style CNN provides a better speech enhancement system and It also outperforms the traditional speech enhancement systems.
[ [<span style="color:blue;">pdf</span>](convolutional_neural_network_based.pdf) ]
[ [<span style="color:green;">code</span>](https://code.com/soheil-khorram/DNN-based-speech-enhancement) ]

* ### Speech Separation





Emotion Recognition
-----------------------------


Mood Recognition
----------------


Statistical Parametric Speech Synthesis
---------------------------------------


Text To Speech
--------------
