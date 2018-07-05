# Image augmentation

There are many ways for augmenting images. In my implementation, keras.preprocessing.image is used and extended to enable new transformations.

## Create image generator from ImageDataFenerator()

Augmenting images is simple with keras. First we need to create an image generator by calling the `ImageDataGenerator()` function and pass it a list of parameters describing the transformations that we want it to perform on the images.

## General steps

### Copy the image.py file

Make a copy of the image.py file on your own machine. You could run `print(keras.__file__)` to print the path to the keras library.

### Edit image.py

- Add attribute for each newly added transformation to the `ImageDataGenerator()` init function.

- Add new functions

- Add IF statement clauses to the `random_transform()` method so that augmentations get implemented when you call `.fit_generator()`

## Train samples using fit_generator()

The final step is to train the CNN and validate the model using `model.fit_generator()` on the real-time augmented images.
