

# ${\color{lightblue} Code \space Snippets}$

This folder provides a few code snippets which are used or are important for the insights of the project. If you want to replicate the entire project I would recommend
having a look at all the notebooks provided in the <b><i> Model </i></b> folder. This folder is mostly for snippets and for someone who wants to get a quick overview of
the working of the project and the approach.

<b><i> Snippet I </i></b>
```java
IMAGE_SHAPE = (224, 224)
Classifier = tf.keras.Sequential([
    hub.KerasLayer("https://tfhub.dev/google/imagenet/mobilenet_v2_130_224/classification/5", input_shape=IMAGE_SHAPE+(3,))    
    # The link is taken from tensorflow hub...
])
```
The <b><i>IMAGE_SHAPE+(3,)</i></b> is used to create the Image of shape <b><i>IMAGE_SHAPE</b></i> with three color channels as the three new dimensions to the Image, since Image comprises of red, green and blue filters (rgb) values.

<b><i> Snippet II </i></b>
```java
daisy[np.newaxis, ...].shape
```
Adding one more dimension, such that the <b><i>classifier does not take one Image and it takes set of Images so</i></b>, we create another dimension for the index.

<b><i> Snippet III </i></b>
```java
eatureExtractor = "https://tfhub.dev/google/imagenet/mobilenet_v2_130_224/feature_vector/5"
ModelWithoutSoftmax = hub.KerasLayer(FeatureExtractor, input_shape=(224, 224, 3), trainable=False)
```
trainable false means we are <b><i>freezing this model</i></b> and this will not br trained further and the pre-defined weights will be used. Except for classification we have feature_vector which gives us the same model except the last layer, like we now have <b><i>no classes pre-defined</i></b> and we can define our own classes.


<b><i> Snippet IV </i></b>
```java
UniqueFlowers = 5
ConvolutionalNeuralNetwork = tf.keras.Sequential([
    ModelWithoutSoftmax,
    tf.keras.layers.Dense(UniqueFlowers)
])
```

Training the network with pre-defined weights as per our use and need. We have five varieties of flowers, so we will use the dense layer with five output neurons.


# ${\color{lightblue} Made \space By}$
<b><i> Vishu Kalier
    
    
    
    
    
    
    
    
