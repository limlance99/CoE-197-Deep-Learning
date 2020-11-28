# Unsupervised MNIST Clustering


### I ended up using Sir Rowel Atienza's code for autoencoding MNIST as the base for my autoencoder:
- link: https://github.com/PacktPublishing/Advanced-Deep-Learning-with-Keras/blob/master/chapter3-autoencoders/autoencoder-mnist-3.2.1.py

I used the following general steps for this notebook:
1) extracted the encoder from the trained autoencoder
2) got the "feature vectors" of x_test to be clustered using K-Means Clustering.
3) Created a bipartite graph by counting the number of occurences of each label on every cluster.
4) Used Hungarian Algorithm on the bipartite graph to get the labels of each cluster.
5) Checked for accuracy by comparing each node's cluster label with its actual label. 

Final Accuracy: 61.87%

