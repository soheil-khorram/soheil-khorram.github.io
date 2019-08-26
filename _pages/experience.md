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

* GAN-based speech enhancement for CI users <font size="-0.5"><span style="color:blue;"><a href="#gan-enhancement">[read more]</a></span></font>
* CNN-based speech enhancement in CI auditory space <font size="-0.5"><span style="color:blue;"><a href="#cnn-enhancement">[read more]</a></span></font>
* Speech separation using probabilistic PIT <font size="-0.5"><span style="color:blue;"><a href="#pit">[read more]</a></span></font>

### Emotion Recognition

* Recognizing continuous emotion labels using MDS network <font size="-0.5"><span style="color:blue;"><a href="#mds-net">[read more]</a></span></font>
* PRIORI Emotion Dataset: a large-scale emotional and conversational speech dataset <font size="-0.5"><span style="color:blue;"><a href="#priori-emd">[read more]</a></span></font>
* Recognizing continuous emotion labels using large receptive field networks <font size="-0.5"><span style="color:blue;"><a href="#lr-nets">[read more]</a></span></font>
* Progressive neural networks for transfer learning in computational paralinguistics <font size="-0.5"><span style="color:blue;"><a href="#pnn">[read more]</a></span></font>
* Multimodal emotion recognition from speech and text <font size="-0.5"><span style="color:blue;"><a href="#multimodal">[read more]</a></span></font>

### Mood Recognition

* Linking mood to emotion detected in-the-wild <font size="-0.5"><span style="color:blue;"><a href="#linking-mood-emotion">[read more]</a></span></font>
* Leveraging cohort and person-specific knowledge in depression recognition <font size="-0.5"><span style="color:blue;"><a href="#cohort">[read more]</a></span></font>

### Text-To-Speech

* Soft context clustering for F0 modeling in HMM-based speech synthesis <font size="-0.5"><span style="color:blue;"><a href="#soft-clustering">[read more]</a></span></font>
* Hidden maximum entropy model for statistical parametric speech synthesis <font size="-0.5"><span style="color:blue;"><a href="#hmem">[read more]</a></span></font>
* Developing text-to-speech systems for the Persian language <font size="-0.5"><span style="color:blue;"><a href="#persian-tts">[read more]</a></span></font>
* Synthesized speech samples <font size="-0.5"><span style="color:blue;"><a href="#synthesized-samples">[read more]</a></span></font>

<br />

---

<br />
<br />
<br />

# Experience

Speech Enhancement/Separation
-----------------------------

<a name="gan-enhancement"></a>
* ### GAN-based speech enhancement for CI users
An important question in developing DNN-based speech enhancement systems for CI users is, what optimization criterion should be used to train the networks? Mean square error (MSE) or log-MSE measures are normally used, but research in CI domain has shown that these measures do not correlate well with the speech intelligibility of CI users. Conditional generative adversarial network (CGAN) provides a solution by replacing the optimization loss functions with a discriminator network. In this project, I am exploring different methods of leveraging CGAN-based architectures to improve the speech intelligibility of CI users. <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>

<a name="cnn-enhancement"></a>
* ### CNN-based speech enhancement in CI auditory space
To improve speech enhancement methods for CI users, I developed a set of convolutional neural network (CNN)-based speech enhancement systems in a cochlear filter-bank feature space, a feature-set specifically designed for CI users based on CI auditory stimuli. In this project, I tested three different CNN architectures: (1) vanilla CNN that directly generates the enhanced signal; (2) spectral-subtraction-style CNN (SS-CNN) that first predicts noise and then generates the enhanced signal by subtracting noise from the noisy signal; (3) Wiener-style CNN that generates an optimal mask for suppressing noise. Results showed that Wiener-style CNN provides a better speech enhancement system and It also outperforms the traditional speech enhancement systems. [<font size="-0.5"><span style="color:blue;">[read more + code]</span></font>](https://github.com/soheil-khorram/DNN-based-speech-enhancement) <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>

<a name="pit"></a>
* ### Speech separation using probabilistic PIT
Probabilistic permutation invariant training (Prob-PIT) improves and extends the conventional PIT for DNN-based speech separation systems. Prob-PIT considers the output-label permutation as a discrete latent random variable with a uniform prior distribution; all possible permutations have the same prior probability. It defines a log-likelihood function based on the prior distributions and the separation errors of all permutations. I showed that this structure can be easily implemented by replacing the minimum function of PIT with a soft-minimum function. Experimental results showed that Prob-PIT provides a smoother optimization landscape in the training phase of the separator network; therefore it can smooth out many local minima of the trining optimization landscape and lead to a better speech separator network. [<font size="-0.5"><span style="color:blue;">[read more + code]</span></font>](https://github.com/soheil-khorram/Prob-PIT) <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>

Emotion Recognition
-----------------------------

<a name="mds-net"></a>
* ### Recognizing continuous emotion labels using MDS network
Continuous emotion labels are generally not synchronized with the input speech signal due to delays caused by reaction-time, which is inherent in human evaluations. In order to train neural networks for continuous emotion recognition, a common method is to first compensate for the reaction-time delays by aligning continuous emotion labels with the speech signals. This approach assumes that the delay compensation and the emotion recognition are independent, yet they significantly depend on each other. To deal with this challenge, I introduced a new convolutional neural network, multi-delay sinc (MDS) network, that is able to simultaneously align and predict labels in an end-to-end manner. The proposed network is a stack of convolutional layers followed by an aligner network that aligns the speech signal and emotion labels. This network is implemented using a new convolutional layer that I introduced, the delayed sinc layer. It is a time-shifted low-pass (sinc) filter that uses a gradient-based algorithm to learn a single delay. I tested the efficacy of this system on two common emotion datasets, RECOLA (AVEC2016) and SEWA (AVEC2017), and showed that this approach obtains state-of-the-art speech-only results by learning time-varying delays while predicting dimensional descriptors of emotions. [<font size="-0.5"><span style="color:blue;">[read more + code]</span></font>](https://github.com/soheil-khorram/MDS-network) <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>

<a name="priori-emd"></a>
* ### PRIORI Emotion Dataset: a large-scale emotional and conversational speech dataset
In this project, I designed and supervised the collection of a new in the wild emotion dataset, the PRIORI Emotion Dataset. This dataset is collected from everyday smartphone conversational speech recordings. The dataset is unique in that it has a high proportion of emotional segments of speech and is the only in the wild telephonic dataset, annotated for emotion. The dataset contains 42 hours of speech with the average of 4 labels per segment. The annotation process of this dataset is ongoing. After annotation concludes, this dataset will be released to the community due to its potential to impact the field of affective computing. [<font size="-0.5"><span style="color:blue;">[read more]</span></font>](../publications/BPD_Emotion.pdf) <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>

<a name="lr-nets"></a>
* ### Recognizing continuous emotion labels using large receptive field networks
In this project, I showed that capturing long-term temporal dependencies is critical for continuous emotion recognition tasks. To do so, I investigated two convolutional neural networks that are efficient in capturing large receptive fields: dilated networks and downsampling/upsampling networks. I showed that even though dilated networks outperform previously reported systems, the output signals produced from such architectures undergo erratic changes between consecutive time steps. This is inconsistent with the slow moving ground-truth emotion labels that are obtained from human annotators. Downsampling/upsampling network deals with this problem by modeling a downsampled version of the input signal and then generate the output signal through upsampling. Not only does the resulting downsampling/upsampling network achieve good performance, it also generates smooth output trajectories. [<font size="-0.5"><span style="color:blue;">[read more]</span></font>](../publications/capturing-long-term.pdf) [<font size="-0.5"><span style="color:blue;">[code]</span></font>](https://github.com/soheil-khorram/neural-network) <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>

<a name="pnn"></a>
* ### Progressive neural networks for transfer learning in computational paralinguistics
Many paralinguistic tasks are closely related and thus representations learned in one domain can be leveraged for another. In this project, I studied how knowledge can be transferred between three paralinguistic tasks: speaker, emotion, and gender recognition. Further, I extended this problem to cross-dataset tasks, asking how knowledge captured in one emotion dataset can be transferred to another. My main focus was on progressive neural networks and I compared these networks to the conventional deep learning methods of pre-training and fine-tuning. Experiments demonstrated that: (1) emotion recognition can benefit from using representations originally learned for different paralinguistic tasks and (2) transfer learning can effectively leverage additional datasets to improve the performance of emotion recognition systems. [<font size="-0.5"><span style="color:blue;">[read more]</span></font>](../publications/progressive.pdf) <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>

<a name="multimodal"></a>
* ### Multimodal emotion recognition from speech and text
In this project, I explored different ways of representing text and also different network architectures for combining text and speech representations. I used two common ways of representing text: (1) word2vec features and (2) a sequence of one-hot vectors that represent word's phonemes. I also tested different neural networks for combining two modalities including feature level and intermediate level fusion techniques. For combining representations obtained from different modalities, I investigated various functions including summation, concatenation, multiplication and outer product functions. [<font size="-0.5"><span style="color:blue;">[paper1]</span></font>](../publications/exploiting_acoustic_and_lexical_properties.pdf) [<font size="-0.5"><span style="color:blue;">[paper2]</span></font>](../publications/pooling.pdf) <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>

Mood Recognition
----------------
<a name="linking-mood-emotion"></a>
* ### Linking mood to emotion detected in-the-wild
Bipolar disorder is a chronic psychiatric illness characterized by pathological mood swings associated with severe disruptions in emotion regulation. Clinical monitoring of mood is key to the care of these dynamic and incapacitating mood states. Speech characteristics change during both depressed and manic states, suggesting automatic methods applied to the speech signal can be effectively used to monitor mood state changes. However, speech is modulated by many factors, which renders mood state prediction challenging. In this project, I used emotion as an intermediary step to improve mood state (depression and mania) prediction. I trained a CNN model for dimensional emotion recognition and showed that the predicted emotion labels have high correlation with both YMRS and HamD measures (YMRS and HamD are two measures that are often used to quantify mood). [<font size="-0.5"><span style="color:blue;">[read more]</span></font>](../publications/BPD_Emotion.pdf) <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>

<a name="cohort"></a>
* ### Leveraging cohort and person-specific knowledge in depression recognition
Mood prediction systems generally assume that the symptomatology of an individual can be modeled using patterns common in a cohort population due to limitations in the size of available datasets. However, individuals are unique. This paper explores person-level systems that can be developed from the current PRIORI database of an extensive and longitudinal collection composed of two subsets: a smaller labeled portion and a larger unlabeled portion. The person-level system employs the unlabeled portion to extract i-vectors, which characterize single individuals. The labeled portion is then used to train person-level and population-level supervised classifiers, operating on the i-vectors and on speech rhythm statistics, respectively. The unification of these two approaches results in a significant improvement over the baseline system, demonstrating the importance of a multi-level approach to capturing depression symptomatology. [<font size="-0.5"><span style="color:blue;">[read more]</span></font>](../publications/depression.pdf) <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>

Text-To-Speech
---------------------------------------
<a name="soft-clustering"></a>
* ### Soft context clustering for F0 modeling in HMM-based speech synthesis
In this project, I proposed and developed a soft decision-tree model that improves the generalization ability of the conventional hard decision-tree structures. The proposed tree is a binary tree with soft decisions at the internal nodes; these internal nodes select both their children with certain membership degrees; therefore, each node can be viewed as a fuzzy set with a context-dependent membership function. soft decision-tree assigns each training sample to multiple overlapped leaves
and therefore it improves model generalization and also provides a better function approximator. I applied the proposed structure in modeling F0 trajectories of a HMM-based speech synthesis system. Both subjective and objective evaluations confirm the superiority of the proposed soft-decision tree over the conventional hard trees. [<font size="-0.5"><span style="color:blue;">[read more]</span></font>](../publications/soft context clustering.pdf) <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>

<a name="hmem"></a>
* ### Hidden maximum entropy model for statistical parametric speech synthesis
Decision tree-clustered context-dependent hidden semi-Markov models (HSMMs) are typically used in HSMM-based speech synthesis to represent probability densities of acoustic features given contextual factors. This project addresses three major limitations of this decision tree-based structure: (1) the decision tree structure lacks adequate context generalization; (2) it is unable to express complex context dependencies. (3) parameters generated from this structure represent sudden transitions between adjacent states. In order to alleviate these limitations, many papers applied multiple decision trees with an additive assumption over those trees. Similarly, in the current project, I used multiple decision trees as well, but instead of the additive assumption, I proposed to train the smoothest distribution by maximizing the entropy measure. Obviously, increasing the smoothness of the distribution improves the context generalization. The proposed model, named hidden maximum entropy model (HMEM), estimates a distribution that maximizes entropy subject to multiple moment-based constraints. All evaluation results of my experiments confirm significant improvement of the proposed system over the conventional HSMM. [<font size="-0.5"><span style="color:blue;">[read more]</span></font>](../publications/context-dependent acoustic.pdf) <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>

<a name="persian-tts"></a>
* ### Developing text-to-speech systems for the Persian language
Scattered and little research in the field of Persian speech synthesis systems has been performed. In this project, I implemented and evaluated several text-to-speech systems for the Persian language. To this end, I designed and supervised the collection process of the ARIANA speech synthesis database containing more than 4 hours of transcribed speech signals. I then developed several speech synthesis systems using the collected dataset including (1) a cluster unit selection speech synthesis using Festival/Festvox/Speech tools, (2) a clustergen statistical parametric speech synthesis, and (3) an HSMM-based speech synthesis with the GV-based parameter generation and the STRAIGHT vocoder. In this project, I also worked on different NLP parts of the Persian TTS including Homograph disambiguation using CRF, letter to phoneme conversion using HMEM, and prosody modeling using CART trees. [<font size="-0.5"><span style="color:blue;">[paper1]</span></font>](../publications/spectral modeling.pdf) [<font size="-0.5"><span style="color:blue;">[paper2]</span></font>](../publications/IMPLEMENTATION AND EVALUATION.pdf) <font size="-0.5"><span style="color:green;"><a href="#top">[back to top]</a></span></font>  

<a name="synthesized-samples"></a>
* ### Synthesized speech samples

Clustergen:

<audio src="../audio/clustergen1.wav" controls></audio>

<audio src="../audio/clustergen2.wav" controls></audio>

<audio src="../audio/clustergen3.wav" controls></audio>

<audio src="../audio/clustergen4.wav" controls></audio>

HTS:

<audio src="../audio/HTS1.wav" controls></audio>

<audio src="../audio/HTS2.wav" controls></audio>

<audio src="../audio/HTS3.wav" controls></audio>

<audio src="../audio/HTS4.wav" controls></audio>

Cluster unit selection:

<audio src="../audio/clunit1.wav" controls></audio>

<audio src="../audio/clunit2.wav" controls></audio>

<audio src="../audio/clunit3.wav" controls></audio>

<audio src="../audio/clunit4.wav" controls></audio>

STRAIGHT:

<audio src="../audio/STRAIGHT1.wav" controls></audio>

<audio src="../audio/STRAIGHT2.wav" controls></audio>

<audio src="../audio/STRAIGHT3.wav" controls></audio>

<audio src="../audio/STRAIGHT4.wav" controls></audio>

Natural:

<audio src="../audio/natural1.wav" controls></audio>

<audio src="../audio/natural2.wav" controls></audio>

<audio src="../audio/natural3.wav" controls></audio>

<audio src="../audio/natural4.wav" controls></audio>

Female DSM:

<audio src="../audio/female1.wav" controls></audio>

<audio src="../audio/female2.wav" controls></audio>

<audio src="../audio/female3.wav" controls></audio>

<audio src="../audio/female4.wav" controls></audio>
