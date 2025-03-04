# Conditional random fields (CRFs) and convolutional neural networks (CNNs) for image segmentation

Here are some resources from the segmentation journal club's June 19, 2018 meeting.

---

## Main paper

[Conditional Random Fields Meet Deep Neural Networks for Semantic Segmentation](http://www.robots.ox.ac.uk/~tvg/publications/2017/CRFMeetCNN4SemanticSegmentation.pdf) \[PDF\]

---

## Presentation figures

All taken from the main paper.

<div class="images"><a href="figs/1%20segmentation%20evolution.png"><img  src="figs/1%20segmentation%20evolution.png" align="center"></a></div>

**1**. Evolution of CNN + CRF segmentation algorithms.

<div class="images"><a href="figs/2%20pascal%20voc.png"><img  src="figs/2%20pascal%20voc.png" align="center"></a></div>

**2**. Pascal VOC 2012 leaderboard (as of January 2018).

<div class="images"><a href="figs/3%20mean-field%20update.png"><img  src="figs/3%20mean-field%20update.png" align="center"></a></div>

**3**. The relationship between CRF pairwise potential choice and the CRF-as-RNN mean-field update equation.

<div class="images"><a href="figs/4%20mean-field%20algorithm.png"><img  src="figs/4%20mean-field%20algorithm.png" align="center"></a></div>

**4**. The CRF-as-RNN mean-field update equation as a neural network module.

<div class="images"><a href="figs/5%20crf%20as%20rnn.png"><img  src="figs/5%20crf%20as%20rnn.png" align="center"></a></div>

**5**. _Top_: High-level schematic of the CRF-as-RNN network. _Bottom_: Comparison of CRF+CNN approaches for a complex segmentation problem.

<div class="images"><a href="figs/6%20mean%20field%20convergence.png"><img  src="figs/6%20mean%20field%20convergence.png" align="center"></a></div>

**6**. Demonstration of the iterative mean field approximation algorithm's convergence.

---


## Important papers

[Efficient inference in fully connected crfs with gaussian edge potentials](http://papers.nips.cc/paper/4296-efficient-inference-in-fully-connected-crfs-with-gaussian-edge-potentials.pdf) \[PDF\]

Introduced DenseCRF.

[DeepLab: Semantic Image Segmentation with Deep Convolutional Nets, Atrous Convolution, and Fully Connected CRFs](https://arxiv.org/pdf/1606.00915.pdf) \[PDF\] 

Describes DeepLabv2, a recent SOTA segmentation algorithm on PASCAL VOC 2012.

[Conditional random fields as recurrent neural networks](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Zheng_Conditional_Random_Fields_ICCV_2015_paper.pdf) \[PDF\]

One of the first two papers to introduce CRF approximation as neural network modules, CRF-RNN.

[Higher order conditional random fields in deep neural networks](https://arxiv.org/pdf/1511.08119.pdf) \[PDF\]

Forming higher-order CRF potentials using object detection and superpixel algorithms.

---

## CRF Implementations

Free Python libraries that should at least work on Linux and OSX.

[pydensecrf](https://github.com/lucasb-eyer/pydensecrf). DenseCRF using Cython. No GPU acceleration, can't learn end-to-end with a neural network module.

#### TensorFlow/Keras

[crfasrnn_keras](https://github.com/sadeepj/crfasrnn_keras). Implements the CRF-as-RNN module, GPU accelerated and trainable.

[Deeplabv2-TensorFlow](https://github.com/zhengyang-wang/Deeplab-v2--ResNet-101--Tensorflow). TensorFlow implementation of DeepLabv2.

[tf.contrib.crf](https://www.tensorflow.org/api_docs/python/tf/contrib/crf). Exists, but looks geared toward CRF usage in NLP, not image processing.

#### Caffe

[crfasrnn](https://github.com/torrvision/crfasrnn). Original implementation of the CRF-as-RNN module. 

[DeepLabv2](http://liangchiehchen.com/projects/DeepLabv2_resnet.html). Original implemenation of DeepLabv2.

#### PyTorch

[DeepLabv2-PyTorch](https://github.com/speedinghzl/Pytorch-Deeplab). PyTorch implementation of DeepLabv2

