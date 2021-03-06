# ![Native2Native](https://github.com/fpark7/Native2Native/blob/master/assets/logo_70.png)
## Native2Native
<br><i>"A Voice and Text Recognition System Built to Specifically for Non-Native Speakers"</i><br>

### About
Our hackathon project for Hack.UVA 2018. [According to the US Census](https://www.census.gov/hhes/socdemo/language/data/acs/PAA_2005_AbilityandEarnings.pdf), there is a high correlation between English speaking ability and employment rate, as well as self-confidence. This clearly puts immigrants and non-native speakers at a disadvantage in the United States. [Image from US Census](https://www.census.gov/hhes/socdemo/language/data/acs/PAA_2005_AbilityandEarnings.pdf)

<a href="url"><img src="https://github.com/fpark7/Native2Native/blob/master/assets/graph.png" align="middle" width=60% ></a>
<br>

Current translating applications are very flawed. First of all, syntax and structure between East-Asian languages and Western languages are completely flipped, making translation an extremely difficult task. In addition, many words and phrases are unique to languages from specific cultures. Because of these two reasons, translations are usually inaccurate and lose information along the way. [Image from here](http://nojeokhill.koreanconsulting.com/2014/02/rethinking-the-korean-localization-process.html)

<a href="url"><img src="https://github.com/fpark7/Native2Native/blob/master/assets/translate.png" align="middle" width=60% ></a>
<br>

However, we have noticed that non-native English speakers know what they want to say; they're just unable to articulate it well. Instead of trying to improve faulty translators, why not start at the imperfect grammar of non-native speakers? Since people are still able to understand broken English, we hypothesize that there will be a lower loss of information from broken English to complete English.
Native2Native is a Natural Language Processor that takes in a "difficult-to-understand" English sentence by a non-native speaker and completes it using Deep Learning, striving to be the "Native" voice for them. (The name "Native2Native" also comes from the Seq2Seq Recurrent Neural Network model used for our application) Unlike most modern speech and text recognition software which rely on translating fluent speech across languages, our solution aims to elevate flawed speech to fluency in the same language.

### Purpose/Vision
Instead of focusing/training Voice-Recognition and Language-Recognition systems solely on eloquent English speech, we should also focus on dedicating them to the people who need these systems the most. In addition, non-native speakers are more likely to learn from corrections to their own English rather than translations of their own native languages. We hope the Native2Native will be a tool to equalize and empower immigrants by offering them a new voice and method to improve use of the English language and will motivate research towards "hard-to-understand" phrases rather than perfect English. Our vision is to generalize our technology and see more Voice-Recognition Models and Language-Translation Models train on data from non-natives rather than native speakers for all languages. 

### Algorithm
Our model trains on "non-native" sentences generated using SpaCy. SpaCy is a power natural language processing library. By labeling linguistic features, tagging parts of speech, and tracing dependencies, we were able to emulate a  clever "non-native speaking" training data set for our neural network. This dataset includes proper sentences that were modified by removing stop-words (common, small words) and swapping nouns with neighboring adjectives or descriptive phrases. In the future, we hope to use real world data and have more time to train our models!

A [Seq2Seq Recurrent Neural Network](https://arxiv.org/pdf/1409.3215.pdf) is used to train on these "non-native/incomplete" sentences and maps them to "complete" sentences. Seq2Seq is an encoder-decoder model that embeds sentences to a higher dimension and then decodes them to a target domain. The model was trained using an [AWS](https://aws.amazon.com/) EC2 P2 instance equipped with a [NVIDIA Tesla K80 GPU](https://www.nvidia.com/en-us/data-center/tesla-k80/). [Image from here](https://google.github.io/seq2seq/) More specifically, our model was a variation of [SimpleText](https://github.com/captainjtx/SimpleText), a RNN that explores the task of simplifying long sentences.

![Translation Model](https://3.bp.blogspot.com/-3Pbj_dvt0Vo/V-qe-Nl6P5I/AAAAAAAABQc/z0_6WtVWtvARtMk0i9_AtLeyyGyV6AI4wCLcB/s1600/nmt-model-fast.gif)
<br>
Our neural network is implemented with [Pytorch](http://pytorch.org/) and deployed using the [SAP Cloud Platform](https://cloudplatform.sap.com/index.html). 

## Developers
Fengyang Zhang <br>
Felix Park <br>
Yutong Wang <br>
Jiten Bhatt <br>

#### Post-Hackathon Notes
We had a great time and we're very proud of the work we completed. We ended up winning "Best Use of Machine Learning to Detect Sponsored Content" sponsored by [Leidos](https://www.leidos.com/). We're not really detecting sponsored content... but I think we received it because we had an interesting approach to a text classification problem. So I guess we'll just call it "Best Use of Machine Learning"? Not mad though :).

Please excuse our bad git commit messages... this was a hackathon. 

We also really wish we had more time training the model. We do not believe 24 hours to code AND train was enough. Although our model showed some powerful results, please do note that its vocabulary is very limited. 

Thank you for checking out this project!



