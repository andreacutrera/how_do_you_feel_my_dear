# how_do_you_feel_my_dear
NLP project for Text Mining and Sentiment Analysis.

Recently, **emotion detection** in text has received attention in the literature on **sentiment analysis**. Detecting emotions is important for studying **human communication in different domains**, including fictional scripts for TV series and movies. The project aims at studying fictional scripts of several movies and TV series under the emotional profile. In particular, the task of the project is threefold:

1. Create a model to predict emotions in text using available datasets as EmoBank or WASSA-2017 or Emotion Detection from Text as training sets (see below);
2. Emotions may be represented either as categorical classes or in a continuous space such as Valence-Arousal-Dominance (see for example Warriner, A. B., Kuperman, V., & Brysbaert, M. (2013). Norms of valence, arousal, and dominance for 13,915 English lemmas. Behavior research methods, 45(4), 1191-1207.)
3. Exploit the model to study an emotional profile of the main characters in one of the movies included in the Cornell Movie--Dialogs Corpus;
4. Study how this emotional profile changes in time along the evolution of the movie story and how it is affected by the various relations among the different characters.

## First model attempts
In the notebook named **text_mining_starting_point.ipynb** you can fetch the data from the WASSA-2017 website, make some initial preprocessing cleaning up the textual documents and make some attempts in models architectures. Data are then saved into the folder named **emotions**.

## Model Selection with few parameters
In the notebook named **text_mining_model_selection.ipynb** you can make a model selection tuning few hyper-parameters, then cross-validating the accuracy of the model.

## Full Model Selection on colab
In the notebook named **text_mining_model_selection-colab.ipynb** you can make a full model selection tuning more hyper-parameters, then cross-validating the accuracy of the model. Then the model architecture and weights learnt are saved into the folder **final_model**. If you want to execute in a 5x times faster press the colab button below.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/16TOIflO9CPvh8WMYQRDCKT6dZ43PHoPM?usp=sharing)

## Preprocess the movie utterances
From the For the movie and TV series dialogues, Cornell Movie-Dialogs Corpus data (https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html) it has been selected the movie: **The Godfather** (1972 - Mario Puzo, Francis Ford Coppola). You can find the preprocessing and utterances extraction from the conversations of the movie selected in the notebook renamed **text_mining_preprocess_movie_data.ipynb**, and also find the final dataset saved with the texts and the characters associated. A further selection has been done on the **main chacarters**: _Don Corleone, Tom Hagen, Michael Corleone, Peter Clemenza and Sonny Corleone_.
