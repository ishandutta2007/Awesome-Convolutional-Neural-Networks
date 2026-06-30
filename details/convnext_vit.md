# The Modern Era: ConvNeXt & Vision Transformer Hybrids

Driven by the rise of Vision Transformers (ViTs), Meta's ConvNeXt (2022) modernized classical CNNs by incorporating modern architectural choices from Transformers.

## Key Design Modifications
- **Inverted Bottlenecks**: Expanding channel dimension in the middle of blocks.
- **Larger Kernels**: Scaling kernel size from $3\times3$ to $7\times7$.
- **Layer Normalization & GELU**: Replacing Batch Normalization and ReLU with more modern alternatives.

### Block Structure
```mermaid
graph TD
    Input[Input] --> DW[7x7 Depthwise Conv]
    DW --> LN[LayerNorm]
    LN --> PW1[1x1 Pointwise Conv / Linear Expand]
    PW1 --> GELU[GELU]
    GELU --> PW2[1x1 Pointwise Conv / Linear Compress]
    PW2 --> Add[Add Skip Connection]
    Input --> Add
```\n