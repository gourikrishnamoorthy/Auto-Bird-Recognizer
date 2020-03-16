## Auto Bird Recogniser using only audio file with Neural Networks
#### Gouri Krishnamoorthy

___

### Summary
This project is a multi-classification supervised learning problem. I downloaded 32GB data from www.xeno-canto.com , 500+ recordings for top 30 birds observed sightings in the state of California USA.

___

Sections:
- [Problem Statement](#Problem-Statement)
- [Challenges](#Challenges)
- [Context](#Context)
- [Goal](#Goal)
- [Importance](#Importance)
- [Data](#Data)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Modeling](#Modeling)
- [Classification Results](#Classification-Results)
- [Web App link](#Web-App-Link)
- [Presentation](#Presentation)
- [Future Steps and Limitations](#Future-Steps-and-Limitations)

___

### Problem Statement
To find out automatic, cheap and unbiased method to reliably identify birds by acoustic monitoring
___

### Challenges
- Multiple simultaneously vocalizing birds
- Non-bird sound (buzzing insects)
- Background noise (wind , rain , etc..)

___

### Context
It is important to gain a better understanding of bird behavior and population trends. Birds respond quickly to environmental change, and may also tell us about other organisms (e.g., insects they feed on), while being easier to detect. Traditional methods for collecting data about birds involve costly human effort. A promising alternative is acoustic monitoring. There are many advantages to recording audio of birds compared to human surveys, including increased temporal and spatial resolution and extent, applicability in remote sites, reduced observer bias, and potentially lower costs. However, it is an open problem for signal processing and machine learning to reliably identify bird sounds in real-world audio data collected in an acoustic monitoring scenario. Some of the major challenges include multiple simultaneously vocalizing birds, other sources of non-bird sound (e.g. buzzing insects), and background noise like wind, rain, and motor vehicles.
The goal in this challenge is to predict the set of bird species that are present given a ten-second audio clip. This is a multi-label supervised classification problem. The training data consists of audio recordings paired with the set of species that are present.

___

### Goal
- Create a robust neural network model that will identify 30 different bird species with at least 70% accuracy
- Create a web app that will take bird sound as input and output predicted bird details

___

### Importance
- Biologists 
- Conservation and Ecology
- General public interested in birding

___

### Data
- Collected list of California birds from wikipedia : https://en.wikipedia.org/wiki/List_of_birds_of_California
- Collected bird sound recordings from : https://www.xeno-canto.org.
This project would not have been possible without the recordings from xeno-canto web site
- Top 30 birds seen in California, 500+ sound files each
- Total data - 32 GB

___

### Exploratory Data Analysis
- EDA included understanding and using python audio packages.
- Mainly used libRosa(https://librosa.github.io/librosa/) functions to analyse audio and feature extraction
- Cleaned up each file to get only the bird sound
- Ran each audio file though all the below treatments:
        
         Chromagram 
         Mel-frequency cepstral coefficients (MFCCs)
         Root-mean-square (RMS) value for each frame
         Spectral centroid
         p’th-order spectral bandwidth
         roll-off frequency
         Zero-crossing rate of an audio time series

___

### Modeling

- Over 3000 features, reduced to 1000 using PCA
- Created a Neural Network model using  1500 epochs

___

### Classification Results

- Robust neural network model that can identify 21 birds with 74% test accuracy. It was able to identify 1380 out of 1874 recordings correctly.

___

### Web App link

   Live App : [Auto Bird Recognizer](https://birding-app.firebaseapp.com/)
   
___

### Presentation 

[Link](Auto_bird_identification_presentation.pdf)


 






