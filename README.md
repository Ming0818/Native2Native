<a href="url"><img src="https://github.com/fpark7/Native2Native/blob/master/assets/logo.PNG" align="left" width="300" ></a>
<br>
<br>
##

### About
Our hackathon project for Hack.UVA 2018. [According to the US Census](https://www.census.gov/hhes/socdemo/language/data/acs/PAA_2005_AbilityandEarnings.pdf), there is a high correlation between English speaking ability and employment rate, as well as self confidence. This clearly puts immigrants and non-native speakers at a disadvantage in the United States. [Image from US Census](https://www.census.gov/hhes/socdemo/language/data/acs/PAA_2005_AbilityandEarnings.pdf)

<a href="url"><img src="https://github.com/fpark7/Native2Native/blob/master/assets/graph.png" align="middle" width=60% ></a>
<br>

Current translating applications are very flawed. First of all, syntax and structure between East-Asian languages and Western languages are completely flipped, making translation a difficult task. Many words from other languages also do not have a direct translation in the English language (and vice versa). [Image from here](http://nojeokhill.koreanconsulting.com/2014/02/rethinking-the-korean-localization-process.html)

<a href="url"><img src="https://github.com/fpark7/Native2Native/blob/master/assets/translate.png" align="middle" width=60% ></a>
<br>

However, we have noticed that non-native English speakers know what they want to say, they're just unable to articulate it well.
Native2Native is a Natural Language Processor that takes in a broken English sentence by a non-native speaker and completes it using Deep Learning... striving to be the "Native" voice for them. (The name "Native2Native" also comes from the Seq2Seq Recurrent Neural Network model used for our application)

### Purpose/Vision
Instead of focusing/training Voice-Recognition and Language-Recognition system on eloquent English speakers, we should focus on dedicating them to the people who need these systems the most. In addition, non-native speakers are more likely to learn from corrections to their own English rather than translations of their own native languages. We hope the Native2Native will be a tool to equalize and empower immigrants by offering them a new voice and method to the English language. 

Our vision is to generalize our technology and see more Voice-Recognition Models and Language-Translation Models train on data from non-natives rather than native speakers for all languages.

### Algorithm
Our naive model trains on "non-native" sentences generated using SpaCy. SpaCy is a power natural language processing library. By labeling linguistic features, tagging parts of speech, and tracing dependencies, we were able to emulate a more clever training data set for our neural network. In the future, we hope to use real world data and have more time to train our models!

A [Seq2Seq Recurrent Neural Network](https://arxiv.org/pdf/1409.3215.pdf) is used to train on these "non-native-incomplete" sentences and maps them to "complete" sentences. [Image from here](https://google.github.io/seq2seq/)

![seq2seq](https://github.com/fpark7/Native2Native/blob/master/assets/seq2seq.gif)
<br>
Our neural network is implemented with [Pytorch](http://pytorch.org/) and deployed using the [SAP Cloud Platform](https://cloudplatform.sap.com/index.html).

## Developers
Fengyang Zhang <br>
Felix Park <br>
Zutong Wang <br>
Jiten Bhatt <br>




