# One-Shot-Classification-using-Siamese-Network-on-MNIST-Dataset

## Dataset
- Used MNIST Dataset dataset from keras

## Siamese Network
- A Siamese Neural Network is a class of neural network architectures that contain two or more identical subnetworks. ‘identical’ here means, they have the same configuration with the same parameters and weights. The two subnetwork outputs an encoding to calculate the difference between the two inputs. The Siamese network's objective is to classify if the two inputs are the same or different using the Similarity score. 

## Loss Functions
In the above python implementation, I calculated the Similarity score using ***Regularized cross-entropy, Contrastive loss function and Triplet loss.***

Accuracy of Siamese Network using different loss functions are:
- Test Accuracy using Contrastive loss : **97.289%**
- Test Accuracy using Triplet Loss : **96.030%**
- Test Accuracy using Regularized Cross Entropy : **55.97%**

Hence, **Contrastive loss is best** among all three loss functions.

## Optimizers
Also I trained the Siamese Network on various optimisers like ***RMSprop, Mini Batch Gradient Descent and Adam Optimizer.***

Accuracy of Siamese Network using different optimizers are:
- Test Accuracy using RMSProp optimizer: **96.189%**
- Test Accuracy using Mini Batch Gradient Descent optimizer: **88.615%**
- Test Accuracy using Adam optimizer: **97.289%**

As we can see that Adam and RMSProp optimizer gave around same accuracies with Adam giving slightly higher. The update rule for Adam is very similar to RMSProp, except we look at the cumulative history of gradients which speeds up the process in case of Adam.

The best optimizer I think is **Adam Optimizer** and the reasons are :
- Adam combines the best properties of RMSProp and AdaGrad to work well even with noisy or sparse datasets.
- Adam is well suited for problems that are large in terms of data and/or parameters.
- Adam is Computationally efficient and has Little memory requirements.
