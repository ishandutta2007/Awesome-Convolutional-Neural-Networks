# The Deep ImageNet Scaling Era: AlexNet to ResNet

This era marked the transition of computer vision from manual feature engineering to deep representation learning, triggered by GPU acceleration and architectural innovations between 2012 and 2015.

## AlexNet (2012)
AlexNet successfully scaled up convolutional networks using GPUs, ReLU activations, and Dropout.

## ResNet (2015)
ResNet introduced **Residual Skip Connections** to solve the vanishing gradient problem, allowing architectures to scale to 100+ layers.

### Residual Block Architecture
```mermaid
graph TD
    X[Input x] --> F[Weight Layer / ReLU / Weight Layer]
    X -->|Skip Connection| Add[Addition: F(x) + x]
    F --> Add
    Add --> Relu[ReLU Activation]
```\n