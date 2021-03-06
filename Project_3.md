For Project Three, I started by downloading the 4 compressed files from slack titled Accra1.zip, Accra2.zip, Accra3.zipand Accra4.zip.  These files contain 10,000 equally sized, high resolution (~60cm), bird’s eye images (orthophotos) of the Korle Gonno neighborhood in Accra. I Also downloaded the file titled labels.csv from the same location.  

I made my initial imports: 

import numpy as np

from numpy import genfromtxt

import glob

from PIL import Image

import tensorflow as tf

from tensorflow.keras.optimizers import RMSprop

from tensorflow.keras.preprocessing.image import ImageDataGenerator

import re


I then built a DNN model, with the purpose testing how well the images are processed.  For this model, I used a batch size of 100, epoch of 100 and a 90 step per epoch in order to get the best MAE I could produce at 35.5106. see data bellow:

Epoch 100/100
90/90 [==============================] - 104s 1s/step - loss: 1591.2548 - mae: 35.5106 - mse: 1591.2548 
___________________________________________________________________________
My test Loss evaluation was: 

32/32 [==============================] - 3s 98ms/step - loss: 2501.2183 - mae: 47.2113 - mse: 2501.2183
One of the issues I found with this model was at times it would overfit, and the MAE would jump up and down. For example, from 37 to 52 in in just two epochs. My largest loss function was 545993.0625 at epoch 5/100, which also would increase and decrease, indicating overfitting. 

_____________________________________________________________________________

Next, I used a much better model for this data set, the CNN model.  This model performed drastically better than the DNN model. In the CNN model, the entire data set ran and with just 5 epochs and the MAE was at 43.299.
Data: 
Epoch 5/5
90/90 [==============================] - 875s 10s/step - loss: 3172.1843 - mae: 43.2999 - mse: 3172.1843

The results show that CNN model performed much better than the DNN as the CNN model  utilized methods such as pooling to maintain the better quality with each epoch, which led to considerable reduction in the MAE.
________________________________________________________________________________

Finally, I wanted to test how well the CNN model would predict the population if I selected three random images. Using the entire data set, I fit the model with batch size of 100, 5 epochs, and 90 training steps per epoch. I tested the 88th, 100th, and 110th image. The results for each are placed below. All though the results were rather unimpressive, I do believe a more dedicated computer could achieve great results using the CNN model.  

## Prediction and Image: 

## Image 88:

![final_p3](https://github.com/Acejv21/Ace_Code/blob/master/final_p3.png?raw=true)

Predicted:0.25877953__ Output:37.3801651000977

## Image: 100

![Pic_p3_100](https://github.com/Acejv21/Ace_Code/blob/master/Pic_p3_100.png?raw=true)

Predicted:0.26262376__Output:  7.98089265823364

## Image:110

![final_3_110](https://github.com/Acejv21/Ace_Code/blob/master/Pic_3_110.png?raw=true)

Predicted: 0.20294054__OutPut: 8.96226596832275
