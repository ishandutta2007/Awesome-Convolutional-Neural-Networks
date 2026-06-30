# Inverted Bottlenecks & Depth Expansion

Inverted Residual blocks (introduced in MobileNetV2) structure internal channel expansions inside residual connections to preserve information capacity.

```mermaid
graph LR
    Input[Narrow Channels] --> Exp[1x1 Conv: Expand Channels]
    Exp --> DW[3x3 Depthwise Conv]
    DW --> Proj[1x1 Conv: Linear Project to Narrow]
    Proj --> Output[Narrow Channels + Skip Connection]
```\n