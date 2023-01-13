# Using Neural Networks on MNIST Dataset

# Problem Statement

Write a neural network that can take 2 inputs:

  an image from MNIST dataset and
  a random number between 0 and 9
  and gives two outputs: the "number" that was represented by the MNIST image, and
                         the "sum" of this number with the random number that was generated and sent as the input to the network
                         
  ![image](https://user-images.githubusercontent.com/63489899/212241343-447d0d62-3042-4797-9d98-6d82823de778.png)
  
  
# Model
  
  ![image](https://user-images.githubusercontent.com/63489899/212242005-b4c9d4c5-a109-4a68-a69e-f6f92b2afbd8.png)

# Loss Function

Because both the MNIST classification and the sum(0-18) are multi class classification problem, I have used Negative Log-Likelihood Loss Function for each of the outputs and averaged the loss:

Loss = (Mnist NLL Loss + Addition NLL Loss)/2

In NLL, the model is punished for making the correct prediction with smaller probabilities and encouraged for making the prediction with higher probabilities. The logarithm does the punishment. NLL does not only care about the prediction being correct but also about the model being certain about the prediction with a high score.

The Pytorch NLL Loss is expressed as: log(x,y) = -log(y) x represents the actual value and y the predicted v

# Training Log

    Epoch 1 : 
    Train set: Average loss: 1.9467
    Val set: Average loss: 1.929, MNist Accuracy:72.58, Sum_Accuracy:10.28

    Epoch 2 : 
    Train set: Average loss: 1.2593
    Val set: Average loss: 1.322, MNist Accuracy:93.14, Sum_Accuracy:13.06

    Epoch 3 : 
    Train set: Average loss: 1.1784
    Val set: Average loss: 1.227, MNist Accuracy:95.52, Sum_Accuracy:17.94

    Epoch 4 : 
    Train set: Average loss: 1.1803
    Val set: Average loss: 1.171, MNist Accuracy:96.42, Sum_Accuracy:23.24

    Epoch 5 : 
    Train set: Average loss: 1.1230
    Val set: Average loss: 1.110, MNist Accuracy:97.2, Sum_Accuracy:32.88

    Epoch 6 : 
    Train set: Average loss: 1.0567
    Val set: Average loss: 1.046, MNist Accuracy:97.6, Sum_Accuracy:39.76

    Epoch 7 : 
    Train set: Average loss: 0.9498
    Val set: Average loss: 0.971, MNist Accuracy:97.96, Sum_Accuracy:49.22

    Epoch 8 : 
    Train set: Average loss: 0.9162
    Val set: Average loss: 0.892, MNist Accuracy:98.14, Sum_Accuracy:59.82

    Epoch 9 : 
    Train set: Average loss: 0.8019
    Val set: Average loss: 0.815, MNist Accuracy:98.28, Sum_Accuracy:74.6

    Epoch 10 : 
    Train set: Average loss: 0.6956
    Val set: Average loss: 0.721, MNist Accuracy:98.24, Sum_Accuracy:78.16

    Epoch 11 : 
    Train set: Average loss: 0.6312
    Val set: Average loss: 0.643, MNist Accuracy:98.56, Sum_Accuracy:86.12

    Epoch 12 : 
    Train set: Average loss: 0.5280
    Val set: Average loss: 0.544, MNist Accuracy:98.48, Sum_Accuracy:92.68

    Epoch 13 : 
    Train set: Average loss: 0.4255
    Val set: Average loss: 0.464, MNist Accuracy:98.72, Sum_Accuracy:93.96

    Epoch 14 : 
    Train set: Average loss: 0.3824
    Val set: Average loss: 0.390, MNist Accuracy:98.64, Sum_Accuracy:96.34

    Epoch 15 : 
    Train set: Average loss: 0.2654
    Val set: Average loss: 0.322, MNist Accuracy:98.8, Sum_Accuracy:97.14

    Epoch 16 : 
    Train set: Average loss: 0.2889
    Val set: Average loss: 0.265, MNist Accuracy:98.86, Sum_Accuracy:98.02

    Epoch 17 : 
    Train set: Average loss: 0.2040
    Val set: Average loss: 0.225, MNist Accuracy:98.86, Sum_Accuracy:98.2

    Epoch 18 : 
    Train set: Average loss: 0.1787
    Val set: Average loss: 0.193, MNist Accuracy:98.88, Sum_Accuracy:98.22

    Epoch 19 : 
    Train set: Average loss: 0.1371
    Val set: Average loss: 0.167, MNist Accuracy:98.74, Sum_Accuracy:98.36

    Epoch 20 : 
    Train set: Average loss: 0.1141
    Val set: Average loss: 0.146, MNist Accuracy:98.8, Sum_Accuracy:98.5
    
 # Inference
 
 ![image](https://user-images.githubusercontent.com/63489899/212243682-9606e258-33fb-4494-bed8-29c40eab4d82.png)

![image](https://user-images.githubusercontent.com/63489899/212243707-6d767fac-54bc-4fb6-99d4-ccbe773c9138.png)

