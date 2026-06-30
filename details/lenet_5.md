# LeNet-5: The Foundational Structural Era

LeNet-5 is a pioneering convolutional neural network architecture proposed by Yann LeCun, Leon Bottou, Yoshua Bengio, and Patrick Haffner in 1998. It was designed primarily for handwritten character and digit recognition.

## Architectural Architecture & Design
LeNet-5 established the classic paradigm of alternating **convolutional layers**, **subsampling (pooling) layers**, and **fully connected layers**.

### Network Structure
```mermaid
graph LR
    Input[Input 32x32 Image] --> C1[Conv Layer C1: 6 maps, 5x5]
    C1 --> S2[Subsampling Layer S2: 2x2 average]
    S2 --> C3[Conv Layer C3: 16 maps, 5x5]
    C3 --> S4[Subsampling Layer S4: 2x2 average]
    S4 --> C5[Conv Layer C5: 120 maps, 5x5]
    C5 --> F6[Fully Connected F6: 84 units]
    F6 --> Output[Output: 10 units]
```

## Key Contributions
- **Local Receptive Fields**: Restricting weight connections to local neighborhoods to capture local spatial features.
- **Shared Weights**: Using the same feature detector kernel across the image to reduce parameter counts and enforce translation invariance.
- **Spatial Subsampling**: Reducing resolution to achieve robustness to minor shifts and distortions.\n