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
I decided to use the siamese network that sir Rowel demonstrated on his github to try and make a good CNN model for CIFAR10. I was not able to maximize the epoch size since I was worried my laptop would die (unfortunately). Based on the trend of the loss graphs however (as seen in the notebooks), the train loss does not stagnate (or plateau) as much as it did with MLP, so I assume that if I were to increase the epochs, the accuracy will surely increase over time.

I ended up doing the same normalization process (shrink to a value of in between -1 to 1) for the RGB values because since I thought it led to improved results with MLP, that it would also lead to improved results for the CNN. Here were my three trial run throughs based on the final model.


### Trials (with each trial being 20 epochs each):
- Trial 1: 58.7%
- Trial 2: 59.9%
- Trial 3: 59.8%

Average accuracy: 59.47%

