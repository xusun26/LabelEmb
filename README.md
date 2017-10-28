# LabelEmb
This is an implementation of the paper [Label Embedding Network: Learning Label Representation for Soft Training of Deep Networks](https://xxx).  
Label Embedding Network can learn label representation (label embedding) during the training process of deep networks. With the proposed method, the label embedding is adaptively and automatically learned through back propagation. The original one-hot represented loss function is converted into a new loss function with soft distributions, such that the originally unrelated labels have continuous interactions with each other during the training process. As a result, the trained model can achieve substantially higher accuracy and with faster convergence speed. Experimental results based on competitive tasks demonstrate the effectiveness of the proposed method, and the learned label embedding is reasonable and interpretable. The proposed method achieves comparable or even better results than the state-of-the-art systems.  
## DataSet
[CIFAR100](https://www.cs.toronto.edu/~kriz/cifar.html), [CIFAR10](https://www.cs.toronto.edu/~kriz/cifar.html) and [MNIST](http://yann.lecun.com/exdb/mnist/).
## Environment and Dependency
- Ubuntu 16.04
- Python 3.5
- Tensorflow 1.3
- Pytorch 0.2.0
## Usage
### CIFAR-100
python3 cifar100.py --mode=baseline  
python3 cifar100.py --mode=emb  
The outputs will be in ./100_results  
### CIFAR-10
python3 cifar10.py --mode=baseline  
python3 cifar10.py --mode=emb  
The outputs will be in ./10_results  
### MNIST
python3 cnn.py --mode=baseline  
python3 cnn.py --mode=emb  
The outputs will be in ./cnn_results  
python3 mlp.py --mode=baseline  
python3 mlp.py --mode=emb  
The outputs will be in ./mlp_results  