

# ${\color{lightblue} Code \space Snippets}$

This folder provides a few code snippets which are used or are important for the insights of the project. If you want to replicate the entire project I would recommend
having a look at all the notebooks provided in the <b><i> Model </i></b> folder. This folder is mostly for snippets and for someone who wants to get a quick overview of
the working of the project and the approach.

# ${\color{red} Snippet \space I}$
```java
IMAGE_SHAPE = (224, 224)
Classifier = tf.keras.Sequential([
    hub.KerasLayer("https://tfhub.dev/google/imagenet/mobilenet_v2_130_224/classification/5", input_shape=IMAGE_SHAPE+(3,))    
    # The link is taken from tensorflow hub...
])
```

# ${\color{lightblue} Made \space By}$
<b><i> Vishu Kalier
