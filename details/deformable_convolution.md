# Deformable Convolution

Deformable Convolution introduces learnable coordinate offsets to the standard rigid grid, enabling kernels to warp dynamically around irregular objects.

```mermaid
graph TD
    Input[Input Feature Map] --> Offset[Offset Field Generator]
    Input --> Conv[Deformable Convolutional Layer]
    Offset -->|Learned Offsets| Conv
    Conv --> Output[Warped / Adaptive Feature Map]
```\n