# 1. Structure of Neural Networks
![image](https://github.com/hyeong01/AI-boostcamp/blob/main/U-stage/Math/images/layers.PNG)
* Repetition of linear transformation and non-linear transformation
* Linear transformation: X -> Z
  * Use of simple mulitplication and addition (aX+b=Z)
* Non-linear transformation: Z -> H
  * Use of activation functions such as ReLU, tanh functions
* Why multi-layer?
  * According to universal approximation theorem, even two-layer neural network can approximate any continous function. However, having more layers allow the model to have less nodes and thus train faster for the same task.
# 2. How Does a Neural Network Train: Back Propagation
![image](https://user-images.githubusercontent.com/38185429/128059638-47d51eac-dafd-4061-a8cf-56eb6a62b829.png)<br/>
* Training == changing the weight of the neural network so that the loss decreases
* If ![image](https://user-images.githubusercontent.com/38185429/128058714-1705d4d2-282c-48a8-acfc-99c4a6aeb3d1.png) is negative then increasing W to an adequate amount will likely decrease the loss. Do the same process for all elements if W is a vector.
* However, ![image](https://user-images.githubusercontent.com/38185429/128058714-1705d4d2-282c-48a8-acfc-99c4a6aeb3d1.png) cannot be calculated on spot. L a function of O, O is a function of H, H in function of Z, ... and Z is a function of W. This is why Why we need a chain rule
* Chain Rule:<br/>
* ![image](https://user-images.githubusercontent.com/38185429/128060222-aa7b43d2-6e79-401e-ace1-00830336fa8f.png) <br/>
![image](https://github.com/hyeong01![Uploading image.png…]()/AI-boostcamp/blob/main/U-stage/Math/images/backpropagation.PNG)
