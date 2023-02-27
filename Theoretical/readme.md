

# ${\color{lightblue} Description}$

# ${\color{red} Transfer \space Learning }$

    Transfer Learning is a technique by which we train a highly dense neural network. The neural network is made to train on
    a very large dataset which could take weeks and months to train. The model is then made to train on the specific or desired
    dataset(s). The trained model usually has a softmax layer as the last hidden layer for classificaton. So we freeze the 
    layers other than the softmax layers. Freezing maintains the weights and kernels as the same as that of the preceded model.
    The last layer is divided into the classes and thus made to classify other set of objects.


# ${\color{red} Benefits}$
 - It mostly used in Image Processing and Classification. Also used as an addictive tool in Computer Vision.
 - It ascertains that the model is well-trained thus, only little fine-tuning of weights is required.
 - The model is also trained in many large datasets and so minimum wastage of parameters is needed.


# ${\color{red} Approach}$
  - I downloaded the pre-trained model from the Tensorflow hub website for the classification of flowers dataset into five categories.
  - The downloaded model has the ability to classify into 1000 categories, not necessarily flowers. The classification is done by the softmax layer as the last hidden layer in the model.
  - The weights and the kernels of all the layers except the last hidden layers are freezed (they are not trained). The softmax layers is changed and we introduce our own classification layer (here classifying into 5 categories).
  - This makes the model run pretty fast, since it has many weights and kernels (non-trainable) which need not to be trained but they help improve the performance and fine-tuning of the model because the model currently has too many parameters.


# ${\color{lightblue} Made \space By}$
 <b><i>Vishu Kalier
