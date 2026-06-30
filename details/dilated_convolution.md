# Dilated / Atrous Convolution

Dilated (or Atrous) convolution introduces gaps into the kernel matrix, allowing a larger receptive field without increasing the number of parameters.

## Mathematical Formulation
For a 1D signal, dilated convolution is formulated as:
$$y[i] = \sum_{k=1}^K x[i + r \cdot k] \cdot w[k]$$
where $r$ is the dilation rate.

```mermaid
graph TD
    Input[Input Grid] -->|Dilation Rate r=2| Kernel[Dilated Kernel / Gaps]
    Kernel --> Output[Expanded Receptive Field]
```\n