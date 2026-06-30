# The Spatial Resolution Loss Dilemma & U-Net

Repeated pooling and stride convolutions reduce spatial resolution, losing fine-grained localization coordinates.

## Solution: U-Net
U-Net uses symmetric encoder-decoder pathways joined by lateral skip connections to preserve spatial details.

```mermaid
graph LR
    Encoder[Encoder Pathway] -->|Skip Connections| Decoder[Decoder Pathway]
    Encoder --> Bottleneck[Bottleneck]
    Bottleneck --> Decoder
```\n