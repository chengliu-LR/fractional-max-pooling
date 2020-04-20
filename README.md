# fractional-max-pooling
This is a reproduction of fractional max pooling method for CNN on MNIST, CIFAR10 and CIFAR100.

In this repo we share our project of reproducing [“Fractional Max-Pooling”](https://arxiv.org/abs/1412.6071), 
Section 4.1 and Section 4.4 of the paper are reproduced.

We reproduced the results of Section 4.1 and 4.4 of the paper. We built a 6 layer FMP network on MNIST and a 12 layer 
FMP network on the CIFAR-100 dataset. A 12 layer FMP network supplemented with dropout and data augmentation was trained 
on the CIFAR-10 dataset. Although there is no open-source code of the network used in this paper, 
we built the network in the same manner as indicated in the paper. The reproduce project was done in the Pytorch 
framework using Google Colaboratory. For the FMP layer, we used the existing function: 
[torch.nn.FractionalMaxPool2d](https://pytorch.org/docs/stable/nn.html#fractionalmaxpool2d). According to the module code of torch.nn, 
the FMP function employs stochastic stride determined by the target output size. 
Since the paper didn’t mention the initialization of hyper-parameter used for training, 
we tuned the hyper-parameter to get the best result we could.
