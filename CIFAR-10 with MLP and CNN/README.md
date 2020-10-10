# CIFAR-10 Modelling with CNN vs MLP

## MLP
I tried multiple different variations to try and get a good percentage, but I could never seem to get out of the 49-51% threshold no matter what I change with the hyper-parameters or the activation functions.

One thing I noticed which gave me a ~1% improvement to my score was normalizing the RGB values into a range of -1 to 1 instead of 0 to 1. I'm honestly not sure why that worked since I was merely testing stuff out but I kept it as it is.

In the end, I decided to try something out (for no real reason) and shaped my MLP into have double the nodes for every single layer (e.g. 256, 512, 1024) before shrinking it back down by a scale of 2 again until I reached the final. This was able to give me the highest accuracy when training.

### Trials (with each trial being 50 epochs each):
- Trial 1: 53.8%
- Trial 2: 54.01%
- Trial 3: 53.9% (uploaded in GitHub)

Average accuracy: 53.90%

## CNN
I decided to use the siamese network that sir Rowel demonstrated on his github to try and make a good CNN model for CIFAR10. I was not able to maximize the epoch size since 


### Trials (with each trial being 50 epochs each):
- Trial 1: 59.8%
- Trial 2: 54.01%
- Trial 3: 53.5%

Average accuracy: 53.77%

