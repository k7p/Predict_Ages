# Face to Age Prediction

This is a project that I completed along with Akshay Tiwari, Stephen Hsu, and David Kes for our Distributed Data graduate data science course.

It utilizes Amazon S3, MongoDB, Spark ML and logistic regression in order to make a prediction of the age of an individual from an image of their face.

We procressed 1.4 GB of data (https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/) that consisted of 124,368 photos, placed this photo data onto Amazon S3, then placed them onto MongoDB, and used an EC2 instance to run the program.

For pre-processing, we had to conver images to their pixel representations, calculated the ages by subtracting the date of birth from the date the photo was taken from the image labels. We also had to filter corrupted images and resize all images to be the same size of 128 x 128 (grayscale) in pre-processing. 

Afterwards, we created a dataframe of the pixel representation of the images along with the label of the true age of the person in the photograph and then fit a logistic regression model to the training data.

After the modeling phase was complete, you can place your own test input images into the model and predict ages from photos of faces.

