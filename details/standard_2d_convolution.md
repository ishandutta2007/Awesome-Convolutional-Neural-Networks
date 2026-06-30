# Standard 2D Convolution

Standard 2D Convolution is the fundamental building block of spatial feature learning in Convolutional Neural Networks.

## Mechanism
A kernel matrix slides across spatial dimensions (height and width) of input feature maps, computing element-wise dot products and summing channel activations.

```mermaid
graph TD
    Input[3D Input Tensor: H x W x C] --> Kernel[Kernel Filters: K x K x C x F]
    Kernel --> Dot[Dot Product + Sum over Channels]
    Dot --> Output[Output Tensor: H_out x W_out x F]
```\n