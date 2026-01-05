### **The Architecture**

!['Unet Architecture](./assets/u-net-architecture.png)

*Image taken from 'U-Net: Convolutional Networks for Biomedical Image Segmentation'* <br>

**U-Net** is a very important network architecture for image segmentation, having several applications, and also several modern variations.<br>

It is similar to an autoencoder, except for the presence of concatenation layers with help the model localize, and give it its U shape. <br>

We can look at the architecture as two components:

1. Encoder block- An encoder block consists of two convolutional layers and one max pooling layer for downsampling. The output from the convolutions is saved for later concatenation, before it is passed to the pooling layer.
2. Decoder block- A decoder block consists of two convolutional layers and one up convolution later for upsampling. Before the convolutions, the previously saved layer is concatenated to the input. <br>

The final mask has per-pixel likelihoods for each class.
