# VIRTUAL-COUNSELOR-WITH-EMOTION-DETECTION
This project presents a BERT based speechbot to counsel people by detecting the emotion of the person from their tone of the voice.

## Idea and Description
The purpose of this project is to develop a counseling speech Bot that can detect the tone of the speaker and provide appropriate responses to comfort their mood swings. This project uses Mel Frequency Cepstral Coefficients (MFCC) to extract features from audio signals and convert them into images. These images are then used to train a deep learning model that can detect emotions from speech. The emotion detected by this model is used as input to a fine-tuned Distil BERT model to generate appropriate responses for the user.

## Steps involved
1.	To develop a system that can convert audio data into image format using MFCC.
2.	To design and train a CNN model that can analyze the MFCC images and identify the user's mood.
3.	To develop a speechbot that can provide appropriate counseling based on the detected mood.
4.	To evaluate the performance of the proposed system in terms of accuracy and effectiveness in counseling users.

## Usage
1. Run the code from the [repository](https://github.com/AMjhagan/Virtual-Counselor-with-emotion-detection/blob/main/audio-emotion-model.ipynb). 
   4 audio datasets are used by this code (audio files along with its labled emotion). The audio from the 4 datasets are combined. Each audio is converted into a MFCC image. The MFCC images are used to train the CNN model to detect the emotion. The [weights](https://github.com/AMjhagan/Virtual-Counselor-with-emotion-detection/blob/main/Emotion_Model.h5) of the CNN model is saved and is later used.

2. The custom made text datasets are used by he speech bot to respond to the user based on the emotion.
   The datasets are : 
   [happy.txt](https://github.com/AMjhagan/Virtual-Counselor-with-emotion-detection/blob/main/happy.txt), 
   [sad.txt](https://github.com/AMjhagan/Virtual-Counselor-with-emotion-detection/blob/main/sad.txt), 
   [angry.txt](https://github.com/AMjhagan/Virtual-Counselor-with-emotion-detection/blob/main/angry.txt), 
   [fear.txt](https://github.com/AMjhagan/Virtual-Counselor-with-emotion-detection/blob/main/fear.txt) and 
   [others.txt](https://github.com/AMjhagan/Virtual-Counselor-with-emotion-detection/blob/main/others.txt). 
   Each dataset consist of common requests and responses for a particular emotion.

3. Run the code from the [repository](https://github.com/AMjhagan/Virtual-Counselor-with-emotion-detection/blob/main/audio-emotion-model.ipynb).
   This code gets the user's voice input. This code then loads the saved [weights](https://github.com/AMjhagan/Virtual-Counselor-with-emotion-detection/blob/main/Emotion_Model.h5) obtained from previous code. It then uses these weights to predict the emotion associated with the voice. After predicting the 
   emotion, its corresponding custom made text dataset is choosen. The input voice is then converted into text. Then BERT based QA pipeline is used to
   generate the response.


## Project group members:
AM Jhagan, VIT Chennai

Jaya Surya S, VIT Chennai

Thamizhmaran N, VIT Chennai

