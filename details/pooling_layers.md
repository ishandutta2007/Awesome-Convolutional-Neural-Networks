# Max & Average Pooling Layers

Pooling layers provide downstream spatial compression and help the network gain translation invariance.

## Comparison
- **Max Pooling**: Selects the peak activation within a grid.
- **Average Pooling**: Calculates the mean activation within a grid.

```mermaid
graph TD
    Input[Input Feature Grid] --> MaxP[Max Pooling: Extracts prominent features]
    Input --> AvgP[Average Pooling: Retains smooth background features]
```\n