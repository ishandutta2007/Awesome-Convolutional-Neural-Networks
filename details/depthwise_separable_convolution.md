# Depthwise Separable Convolution

Depthwise Separable Convolutions partition a standard convolution into two distinct steps to maximize parameter efficiency:

1. **Depthwise Convolution**: Apply a single filter per channel.
2. **Pointwise Convolution**: Apply a $1\times1$ convolution to combine channel features.

```mermaid
graph TD
    Input[Input: H x W x C] --> DW[Depthwise Conv: C Filters of K x K x 1]
    DW --> Inter[Intermediate: H x W x C]
    Inter --> PW[Pointwise Conv: F Filters of 1 x 1 x C]
    PW --> Output[Output: H x W x F]
```\n