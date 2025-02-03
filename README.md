# Phishing Website Detection by Machine Learning Techniques
## Interface


![Screenshot 2025-02-03 194308](https://github.com/user-attachments/assets/cb11345f-29b7-4cd1-b476-e1f2abc7d2a8)
![Screenshot 2025-02-03 194159](https://github.com/user-attachments/assets/2075bd65-6d0c-4a04-87ef-a5762c9427ae)

## Project Goal:
We're building a smart system to catch fake websites that try to steal your information. These fake sites often look just like real banking or shopping websites to trick people. We're using artificial intelligence and machine learning to automatically spot these dangerous copycats before they can harm anyone.
# How We're Doing It:
# Data Gathering:
We collected 5,000 known fake website addresses from PhishTank, a trusted source that tracks phishing scams
We also gathered 5,000 legitimate website addresses from the University of New Brunswick's database
This balanced mix helps our AI learn the difference between real and fake sites
# Training Our AI:
We teach our computer models to spot telltale signs of fake websites
The AI learns patterns in website addresses and page content
It gets better at distinguishing between legitimate and dangerous sites over time
Think of it like teaching a security guard to spot fake IDs - the more examples they see, the better they get at catching the fakes. Our AI works the same way, but it can check thousands of websites in seconds to keep users safe from scams.
This project is especially relevant for banks like Union Bank of India, as it helps protect both the institution and its customers from phishing attacks.
## Feature Extraction
The below mentioned category of features are extracted from the URL data:

1.   Address Bar based Features <br>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In this category 9 features are extracted.
2.   Domain based Features<br>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In this category 4 features are extracted.
3.   HTML & Javascript based Features<br>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In this category 4 features are extracted.



## Models & Training

Before stating the ML model training, the data is split into 80-20 i.e., 8000 training samples & 2000 testing samples. From the dataset, it is clear that this is a supervised machine learning task. There are two major types of supervised machine learning problems, called classification and regression.

This data set comes under classification problem, as the input URL is classified as phishing (1) or legitimate (0). The supervised machine learning models (classification) considered to train the dataset in this project are:

* Decision Tree
* Random Forest
* Multilayer Perceptrons
* XGBoost
* Autoencoder Neural Network
* Support Vector Machines

All these models are trained on the dataset and evaluation of the model is done with the test dataset. The elaborate details of the models & its training are mentioned in [Phishing Website Detection_Models & Training.ipynb](https://github.com/shreyagopal/Phishing-Website-Detection-by-Machine-Learning-Techniques/blob/master/Phishing%20Website%20Detection_Models%20%26%20Training.ipynb)[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyagopal/Phishing-Website-Detection-by-Machine-Learning-Techniques/blob/master/Phishing%20Website%20Detection_Models%20%26%20Training.ipynb)



## End Results
From the obtained results of the above models, XGBoost Classifier has highest model performance of 86.4%. So the model is saved to the file '[XGBoostClassifier.pickle.dat](https://github.com/shreyagopal/Phishing-Website-Detection-by-Machine-Learning-Techniques/blob/master/XGBoostClassifier.pickle.dat)'

### Next Steps

This project can be further extended to creation of browser extention or developed a GUI which takes the URL and predicts it's nature i.e., legitimate of phishing. *As of now, I am working towards the creation of browser extention for this project. And may even try the GUI option also.* The further developments will be updated at the earliest. 
