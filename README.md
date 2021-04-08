# DeepfakeDetection
Deepfakes represent AI generated videos of people doing or saying fictional things by generating or replacing faces. This can be used for carrying out malicious and criminal practices such as evidence tampering, political manipulation, etc. With limited effort and simple equipment like smartphones, many new devices accessible on the Web have made it simpler than ever for anybody to create practical ”deepfakes.” Apps are released to public to create their own fake images or videos, e.g., FaceApp and ZAO.
Our goal is to create a deep learning model that is capable of recognizing deepfake videos.

DATASET: 

The dataset used is the deepfake detection challenge dataset available on Kaggle.

The size of dataset downloaded is 4.13 GB, and the dataset is divided into training and test samples, each containing 400 videos.

The training dataset is divided in the ratio of 80:20 for fake vs real.


PROPOSED SOLUTION: 

1.   Pre-process the data: ​
Divide video into frames​
Face detection and crop face from all frames​
Store the cropped face images in a new directory​

2.   Modelling: ​
InceptionResNet-v2 is used as a pretrained model.​
The initial algorithm produces 64x64 pixel images. We resize them into 128x128 pixel images.​
Activation function – SoftMax, Loss function – Binary cross-entropy, Optimization function- Adam.​

3.   Evaluation: ​
Training and validation accuracy and loss​
Confusion Matrix​


CONCLUSION: 

Our project uses InceptionResNet-V2 transfer learning model, which is trained on massive image datasets as the pre-trained model. ​

The evaluation  shows that the model trained on 400 short video dataset can achieve 91.19% validation accuracy with validation loss of 31.18%. Test accuracy = 99.52%, loss = 1.82%​

Confusion Matrix results: True Positive = 2943, True Negative = 718, False positive = 43, False Negative = 41

With high-end computation power and more storage , a much more advanced model can be developed, which can take bigger videos in the input. ​
