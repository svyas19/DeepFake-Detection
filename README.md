# DeepFake-Detection


![Obama Deep Fake](https://github.com/svyas19/DeepFake-Detection/blob/main/Obama%20Deep%20Fake.gif)</br>
</t></t>Real</t></t></t></t>Fake

## 1. Objective & DeepFakes</br></br>

The objective of this project is to detect if anything is wrong with a video or image i.e. to classify between “REAL” and “FAKE”.</br> 
A deepfake refers to a specific kind of synthetic media where a person in an image or video is swapped with another person's likeness. </br>
The deepfake uses the neural network techniques in such an accurate and perfect way that it is almost impossible for a naked human eye to differentiate between the real and the fake videos/Images.</br></br>

The following image shows a comparison between DeepFake and Orignal Image, it is really difficult to identify which one is original and which one is fake with the naked eye.</br></br>

![Obama DeepFakes](https://github.com/svyas19/DeepFake-Detection/blob/main/Auto-Encoder%201.png)</br>


## 2.Introduction</br></br>

### How Deep Fakes are created?</br>

The initial step is to gather the face data, by finding the videos/images of the source person and target whose deepfake is to be created.</br>
Faces are located and extracted from these data, it can be done using some of the pre-trained models for face detection such as MT-CNN, FaceNet, etc.</br>
Autoencoder is used to compress and decompress the facial features.</br>
This helps the model to perfectly learn how to store the facial features of the source and target.</br>

![Autoencoder 1](https://github.com/svyas19/DeepFake-Detection/blob/main/Auto-Encoder%201.png)</br>

Then, a common decoder is used to substitute the decoder for source and target.</br>

![Autoencoder 2](https://github.com/svyas19/DeepFake-Detection/blob/main/Auto-Encoder%202.png)</br>

### 3. Why is Detection of DeepFake Important?</br></br>

Researchers are considering DeeFakes as the most dangerous crime of the future as they have the ability to modify the information in the most believable way.</br>

Some areas where DeepFakes are used in a malicious way : </br>
Fake News</br>
Evidence Tampering</br>
Political Manipulation</br>
Revenge Porn</br>
Financial Fraud</br></br>

Basically, DeepFake can provide control over billions of people by making them believe whatever you want.</br>
Deep fakes are not just limited to videos, audio can also be manipulated too.</br>

Some Real-World implementations of DeepFakes:</br>

President Barack Obama Speech </br>
Tom Cruise as Iron Man</br>
Joe as President Trump </br>

![Project Overview](https://github.com/svyas19/DeepFake-Detection/blob/main/DeepFake%20Project%20Overview.png)</br>

### 4. Data Preprocessing:</br></br>

The data was in form of videos and I needed to extract the faces from each video from the frames in the video:</br>

#### Extracting Frames from Videos </br>
Using OpenCV, every 10th(considering computational power)  frame from each video was extracted:</br>

![Deep Fake1](https://github.com/svyas19/DeepFake-Detection/blob/main/Deepfake%201.png)</br>


### Extracting Faces from frames:</br>
Faces were extracted from the frames using two methods:</br>
A)Using FaceNet Pretrained Model</br>
B) OpenCV Deep Learning Model </br>


![DeepFake 2](https://github.com/svyas19/DeepFake-Detection/blob/main/DeepFake%202.png)</br>


#### 5. CNN Architectures :</br>

Different CNN Architectures were tested to see how they perform.</br>
Following CNN Architectures were tested :</br>

![CNN Architectures](https://github.com/svyas19/DeepFake-Detection/blob/main/CNN%20Architectures.png)</br>


### 6. Ensemble</br></br>

MiniVGGNet, LeNet, and ResNet showed relatively high accuracy from others after tuning the hyperparameters and trying different combinations of architectures.</br>

Different Ensemble learning tested with different Nets:</br>

![Ensembles](https://github.com/svyas19/DeepFake-Detection/blob/main/Ensembles.png)</br>


### 7.Final Model Results</br>
Highest Accuracy : 99%</br>
Net: LeNet</br>
Kernel Regularizer L1 = le-10 </br>
Activity Regularizer L2 = le-07</br>
Optimizer: Adam	</br>
Activation : ReLu</br>
Loss: Categorical_Crossentropy</br>
Padding: Same </br>
Stride : (2,2)</br></br>

![Highest Accuracy](https://github.com/svyas19/DeepFake-Detection/blob/main/Highest_accuracy.png)</br></br>

### 8. Model Deployment</br>

Research shows that 90% of the developed models never get deployed.</br>
Considering this, the model was deployed as a web application using Flask, Ngrok, HTML, and CSS.</br></br>

Using Deployed Model:</br>

Open the Web Application:</br>

Start the server:</br>
![Server](https://github.com/svyas19/DeepFake-Detection/blob/main/Server.png)</br>

Open the Web Application:</br>
![Input](https://github.com/svyas19/DeepFake-Detection/blob/main/Input.png)</br>

Provide the Input and Get Predictions:</br>
![Output](https://github.com/svyas19/DeepFake-Detection/blob/main/Output.png)</br>







