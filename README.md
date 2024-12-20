# Harmful-ECA-rules-classifiers



This repository contains the supplementary material for the paper "Identifying Security and Privacy Violation Rules in Trigger-Action IoT Platforms with NLP Models" published in the IEEE Internet of Things Journal.

This material comprises the dataset employed to train the classification models and the source codes useful for the repeatability of the experiments.

## Download
The dataset can be downloaded by sending an email to one of the authors.<br>
This dataset should be used for academic non-commercial purposes only. Any other usage is prohibited according to the IFTTT Terms of Service. <br>


<p align="center">
  <img width="350" height="500"
    src="https://github.com/empathy-ws/Risky-IFTTT-applets-classifiers/blob/main/lockTAP.png"
  >
</p>

# Creators

Bernardo Breve (bbreve@unisa.it), Gaetano Cimino (gcimino@unisa.it), Vincenzo Deufemia (deufemia@unisa.it)

University of Salerno

# Dataset Information

The original dataset [1] (<a href="https://www-users.cse.umn.edu/~fengqian/ifttt_measurement/">download</a>) composed of unlabeled applets was partitioned into two sets of data, which were go through two separate processes: while a random small set of applets was manually labeled, the remaining larger set of unlabeled applets managed to be labeled through an automatic process. In fact, we considered three semi-supervised classification models which exploit the set of labeled applets to acquire sufficient knowledge for providing the labels to the applets contained in the larger set. Then, an ensemble approach was employed to establish, among the labels provided by the semi-supervised models, which should be the label to be assigned to each applet, yielding a final large dataset of applets labeled according to the four classes of risk.

<table align="center">
    <tr>
     <td align="center"><b>Dataset Characteristics:</td>
        <td align="center"><i>Multi-class</td>
        <td align="center"><b>Number of instances:</td>
        <td align="center"><i>79214</td>
    </tr>
    <tr>
        <td align="center"><b>Attribute Characteristics:</td>
        <td align="center"><i>Categorical</td>
        <td align="center"><b>Number of attributes:</td>
        <td align="center"><i>7</td>
    </tr>
    <tr>
        <td align="center"><b>Associated Tasks:</td>
        <td align="center"><i>Classification</td>
        <td align="center"><b>Number of classes:</td>
        <td align="center"><i>4</td>
    </tr>
</table>

## Training set: 
Dataset of IFTTT applets labeled with respect to security and privacy risks by using an ensemble of three semi-supervised learning techniques (Self Learning, Label Propagation, and Generative Adversarial Learning).
#### Number of instances: 
76741

## TS_2k: 
Dataset of manually labeled IFTTT applets. 
#### Number of instances: 
2473

## TS_500:
Dataset of manually labeled IFTTT applets obtained by randomly selecting applets among those discarded by the ensemble approach (i.e., the applets that obtained conflicting predictions by the three semi-supervised techniques).
#### Number of instances:
500

## TS_425:
Dataset of manually labeled IFTTT applets obtained by removing the inconsistent applets from the random set.
#### Number of instances:
425

# Attribute Information

<table align="center">
    <tr>
        <td align="center"><b>TriggerTitle:</td>
        <td align="center">is a string representing the name of the trigger that activates the applet</td>
    </tr>
    <tr>
        <td align="center"><b>TriggerChannelTitle:</td>
        <td align="center">is a string representing the name of the trigger channel chosen by the user as a trigger for the applet</td>
    </tr>
    <tr>
        <td align="center"><b>ActionTitle:</td>
        <td align="center">is a string representing the name of the action to execute in response to the trigger</td>
    </tr>
    <tr>
        <td align="center"><b>ActionChannelTitle:</td>
        <td align="center">is a string representing the name of the action channel chosen as an action by the user</td>
    </tr>
    <tr>
        <td align="center"><b>Title:</td>
        <td align="center">is a string containing the title of the applet</td>
    </tr>
    <tr>
        <td align="center"><b>Desc:</td>
        <td align="center">is a string containing a description of the applet's behavior</td>
    </tr>
    <tr>
        <td align="center"><b>Target:</td>
        <td align="center">is a number representing the damage class</td>
    </tr>
</table> 

# Models Information

We considered two types of classifiers. The first, based on Artificial Neural Networks, treats discrete features (TriggerTitle, TriggerChannelTitle, ActionTitle, and ActionChannelTitle) as numerical values, using the label encoder technique, and the continuous features (Title and Desc) as textual values, using a word embedding technique, namely Global Vectors for Word Representation. The second is based on BERT (Bidirectional Encoder Representations from Transformers), a pre-training model of natural language processing, which uses deep bidirectional transformers to train a language representation model through a large number of data. For this model, all features were treated as text.

# Relevant Papers

[1] Mi, X., Qian, F., Zhang, Y., Wang, X., 2017. An empirical characterization of IFTTT: ecosystem, usage, and performance, in: Proceedings of the Internet Measurement Conference, ACM. pp. 398–404

# Citation 

```
@article{breve2022identifying,
  title={Identifying Security and Privacy Violation Rules in Trigger-Action IoT Platforms with NLP Models},
  author={Breve, Bernardo and Cimino, Gaetano and Deufemia, Vincenzo},
  journal={IEEE Internet of Things Journal},
  year={2022},
  publisher={IEEE}
}
```
