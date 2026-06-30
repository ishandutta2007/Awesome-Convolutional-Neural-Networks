# Squeeze-and-Excitation (SE) Attention Blocks

Squeeze-and-Excitation blocks adaptively recalibrate channel-wise feature responses by explicitly modeling interdependencies between channels.

```mermaid
graph TD
    Input[Input Tensor: H x W x C] --> Squeeze[Squeeze: Global Average Pooling]
    Squeeze --> Excitation[Excitation: Fully Connected layers + Sigmoid]
    Excitation --> Scale[Scale Channels of Input]
    Input --> Scale
```\n