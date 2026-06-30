# The GPU Memory-Bandwidth Boundary & Activation Checkpointing

Training deep neural networks requires storing intermediate activations during the forward pass to compute gradients during the backward pass, leading to activation bloat.

## Solution: Activation Checkpointing
Store only select boundary activations and recompute the intermediate ones during the backward pass.

```mermaid
graph TD
    Forward[Forward Pass] -->|Store Checkpoints Only| HBM[High Bandwidth Memory]
    Backward[Backward Pass] -->|Recompute Intermediate Activations| Backprop[Gradient Computation]
    HBM --> Backprop
```\n