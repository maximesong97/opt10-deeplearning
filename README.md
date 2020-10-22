# opt10-deeplearning

I first start by adding complexity to the model with more convolution layers.
Each convolution layer doubles the number of filters.
I added convolution layers until we couldn't improve the performance by simply adding more complexity.
With more complexity, it takes longer to train, so i fixed the number of epoch to 25.
And after a certain time, when i have trained the model enough to observe overfitting, i put a dropout layer with p=0.5 on the first fully connected layer.
I increase the number of neurons on the first fully connected layer since we have much more output values from the last conv layer.

Each filter was of size 3 which is the most used size for filter.
I kept the dimension by doing a padding of 1 and instead i used the maxpooling layer to decrease the dimension.

Batch size = 32
Number of epoch = 25
Learning rate = 0.001

Final number of feature maps = 576
Number of convolution layers = 6
Size of the fully connected layer = 128

Accuracy of the network on the 10000 test images: 67.36 %

When observing the courb, we see that we are overfitting on the training data while losing generalisation power (increase of the loss on validation set).
