## Welcome to DeepNAT - Deep Convolutional Neural Network for Segmenting Neuroanatomy

### What is DeepNAT?

We introduce DeepNAT, a 3D Deep convolutional neural network for the automatic segmentation of NeuroAnaTomy in
T1-weighted magnetic resonance images. DeepNAT is an end-to-end learning-based approach to brain segmentation that
jointly learns an abstract feature representation and a multi-class classication. We propose a 3D patch-based approach,
where we do not only predict the center voxel of the patch but also neighbors, which is formulated as multi-task learning.
To address a class imbalance problem, we arrange two networks hierarchically, where the rst one separates foreground
from background, and the second one identies 25 brain structures on the foreground. Since patches lack spatial
context, we augment them with coordinates. To this end, we introduce a novel intrinsic parameterization of the brain
volume, formed by eigenfunctions of the Laplace-Beltrami operator. As network architecture, we use three convolutional
layers with pooling, batch normalization, and non-linearities, followed by fully connected layers with dropout. The nal
segmentation is inferred from the probabilistic output of the network with a 3D fully connected conditional random eld,
which ensures label agreement between close voxels. The roughly 2.7 million parameters in the network are learned with
stochastic gradient descent. Our results show that DeepNAT compares favorably to state-of-the-art methods. Finally,
the purely learning-based method may have a high potential for the adaptation to young, old, or diseased brains by
ne-tuning the pre-trained network with a small training sample on the target application, where the availability of
larger datasets with manual annotations may boost the overall segmentation accuracy in the future.

### Requirements


For running DeepNAT segmentation we used a modified version of the deep learning framework [caffe](http://caffe.berkeleyvision.org/), which you can find [here](https://github.com/TJKlein/caffe).


### Trained Model files

Available shortly
