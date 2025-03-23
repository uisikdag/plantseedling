# Weed Classification Model Benchmark Report with Stratified 5-Fold Cross-Validation

## Dataset Information

- Total samples: 3000
- Training+Validation samples: 2700
- Test samples: 300
- Classes: Black-grass, Charlock, Cleavers, Common Chickweed, Common wheat, Fat Hen, Loose Silky-bent, Maize, Scentless Mayweed, Shepherds Purse, Small-flowered Cranesbill, Sugar beet

## Training Results

- Cross-validation: Stratified 5-fold

- Accuracy,Precision,Recall,F1-Score are calculated based on Test Set

- Best Validation Accuracy is calculated as the accuracy of the fold with best value

- Average Per Class Performance for each fold is calculated as the mean of Test Set results for all folds

-Std Dev refers to the standard deviation of the Test Accuracy across different folds in the cross-validation process. 

## Model Performance Comparison

| Model               |   Accuracy |   Precision |   Recall |   F1-Score |   Best Val Acc |   Parameters (M) |   Std Dev |   Completed Folds |
|:--------------------|-----------:|------------:|---------:|-----------:|---------------:|-----------------:|----------:|------------------:|
| swinv2              |      97.4  |       97.56 |    97.4  |      97.4  |          97.3  |            86.91 |      0.65 |                 5 |
| convnext_large      |      97.33 |       97.45 |    97.33 |      97.33 |          97.74 |           196.25 |      0.6  |                 5 |
| nasnet_large        |      97.07 |       97.32 |    97.07 |      97.06 |          97.37 |            84.77 |      0.39 |                 5 |
| mobilenet_v3        |      96.93 |       97.13 |    96.93 |      96.93 |          97.04 |             4.22 |      0.25 |                 5 |
| davit               |      96.87 |       97.01 |    96.87 |      96.87 |          97.78 |            86.94 |      1.09 |                 5 |
| efficientnet_v3     |      96.73 |       96.83 |    96.73 |      96.73 |          97.11 |            20.19 |      0.71 |                 5 |
| inception_resnet_v2 |      96.67 |       96.83 |    96.67 |      96.68 |          97.59 |            54.32 |      0.6  |                 5 |
| resnet152           |      96.53 |       96.72 |    96.53 |      96.52 |          96.96 |            58.17 |      0.4  |                 5 |
| vgg19               |      95.47 |       95.6  |    95.47 |      95.47 |          95.44 |           139.63 |      0.81 |                 5 |
| coatnet_3           |      90.13 |       90.65 |    90.13 |      90.11 |          89.67 |           163.65 |      3.67 |                 5 |
| vit_large_patch16   |      58.33 |       59.71 |    58.33 |      56.92 |          61.56 |           303.31 |     17.5  |                 5 |

## Individual Model Results

### vgg19

#### Architecture Details
- Total Parameters: 139,630,412

#### Cross-Validation Results

| Fold | Best Val Acc | Test Acc | Precision | Recall | F1-Score |
|------|-------------|----------|-----------|--------|----------|
| 1 | 95.56% | 95.33% | 95.41% | 95.33% | 95.31% |
| 2 | 95.19% | 94.33% | 94.39% | 94.33% | 94.32% |
| 3 | 95.00% | 96.00% | 96.28% | 96.00% | 96.03% |
| 4 | 95.19% | 96.67% | 96.78% | 96.67% | 96.67% |
| 5 | 96.30% | 95.00% | 95.12% | 95.00% | 95.02% |
| **Avg** | **95.44%** | **95.47% ± 0.81%** | **95.60%** | **95.47%** | **95.47%** |

#### Average Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Black-grass | 81.20% | 86.40% | 83.71% |
| Charlock | 100.00% | 100.00% | 100.00% |
| Cleavers | 100.00% | 96.00% | 97.96% |
| Common Chickweed | 95.44% | 100.00% | 97.66% |
| Common wheat | 92.05% | 97.60% | 94.64% |
| Fat Hen | 96.94% | 94.40% | 95.59% |
| Loose Silky-bent | 87.82% | 80.80% | 84.15% |
| Maize | 99.23% | 100.00% | 99.61% |
| Scentless Mayweed | 99.20% | 97.60% | 98.38% |
| Shepherds Purse | 97.60% | 96.80% | 97.18% |
| Small-flowered Cranesbill | 97.69% | 100.00% | 98.82% |
| Sugar beet | 100.00% | 96.00% | 97.94% |

---

### resnet152

#### Architecture Details
- Total Parameters: 58,168,396

#### Cross-Validation Results

| Fold | Best Val Acc | Test Acc | Precision | Recall | F1-Score |
|------|-------------|----------|-----------|--------|----------|
| 1 | 96.67% | 97.00% | 97.43% | 97.00% | 96.97% |
| 2 | 96.85% | 96.33% | 96.57% | 96.33% | 96.32% |
| 3 | 97.04% | 97.00% | 97.08% | 97.00% | 97.00% |
| 4 | 97.41% | 96.33% | 96.44% | 96.33% | 96.33% |
| 5 | 96.85% | 96.00% | 96.07% | 96.00% | 96.00% |
| **Avg** | **96.96%** | **96.53% ± 0.40%** | **96.72%** | **96.53%** | **96.52%** |

#### Average Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Black-grass | 84.13% | 91.20% | 87.30% |
| Charlock | 100.00% | 100.00% | 100.00% |
| Cleavers | 100.00% | 96.00% | 97.96% |
| Common Chickweed | 94.73% | 100.00% | 97.29% |
| Common wheat | 95.41% | 99.20% | 97.25% |
| Fat Hen | 100.00% | 94.40% | 97.11% |
| Loose Silky-bent | 91.01% | 82.40% | 86.18% |
| Maize | 99.23% | 100.00% | 99.61% |
| Scentless Mayweed | 99.20% | 96.80% | 97.98% |
| Shepherds Purse | 96.89% | 99.20% | 98.02% |
| Small-flowered Cranesbill | 100.00% | 100.00% | 100.00% |
| Sugar beet | 100.00% | 99.20% | 99.59% |

---

### inception_resnet_v2

#### Architecture Details
- Total Parameters: 54,324,908

#### Cross-Validation Results

| Fold | Best Val Acc | Test Acc | Precision | Recall | F1-Score |
|------|-------------|----------|-----------|--------|----------|
| 1 | 98.15% | 97.00% | 97.15% | 97.00% | 97.00% |
| 2 | 97.78% | 96.33% | 96.67% | 96.33% | 96.38% |
| 3 | 96.48% | 97.00% | 97.14% | 97.00% | 97.01% |
| 4 | 97.78% | 97.33% | 97.44% | 97.33% | 97.33% |
| 5 | 97.78% | 95.67% | 95.75% | 95.67% | 95.66% |
| **Avg** | **97.59%** | **96.67% ± 0.60%** | **96.83%** | **96.67%** | **96.68%** |

#### Average Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Black-grass | 84.99% | 94.40% | 89.41% |
| Charlock | 100.00% | 100.00% | 100.00% |
| Cleavers | 100.00% | 96.00% | 97.96% |
| Common Chickweed | 93.30% | 100.00% | 96.53% |
| Common wheat | 93.81% | 96.00% | 94.87% |
| Fat Hen | 99.17% | 92.80% | 95.87% |
| Loose Silky-bent | 93.00% | 84.80% | 88.71% |
| Maize | 97.69% | 100.00% | 98.82% |
| Scentless Mayweed | 100.00% | 100.00% | 100.00% |
| Shepherds Purse | 100.00% | 100.00% | 100.00% |
| Small-flowered Cranesbill | 100.00% | 100.00% | 100.00% |
| Sugar beet | 100.00% | 96.00% | 97.94% |

---

### mobilenet_v3

#### Architecture Details
- Total Parameters: 4,217,404

#### Cross-Validation Results

| Fold | Best Val Acc | Test Acc | Precision | Recall | F1-Score |
|------|-------------|----------|-----------|--------|----------|
| 1 | 97.78% | 96.67% | 97.22% | 96.67% | 96.62% |
| 2 | 96.48% | 96.67% | 96.81% | 96.67% | 96.67% |
| 3 | 96.67% | 97.00% | 97.09% | 97.00% | 97.01% |
| 4 | 97.41% | 97.33% | 97.45% | 97.33% | 97.33% |
| 5 | 96.85% | 97.00% | 97.09% | 97.00% | 97.01% |
| **Avg** | **97.04%** | **96.93% ± 0.25%** | **97.13%** | **96.93%** | **96.93%** |

#### Average Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Black-grass | 85.82% | 94.40% | 89.78% |
| Charlock | 100.00% | 100.00% | 100.00% |
| Cleavers | 100.00% | 96.00% | 97.96% |
| Common Chickweed | 94.02% | 100.00% | 96.91% |
| Common wheat | 96.98% | 99.20% | 98.04% |
| Fat Hen | 100.00% | 94.40% | 97.11% |
| Loose Silky-bent | 94.06% | 84.00% | 88.50% |
| Maize | 100.00% | 100.00% | 100.00% |
| Scentless Mayweed | 99.23% | 97.60% | 98.38% |
| Shepherds Purse | 97.69% | 99.20% | 98.42% |
| Small-flowered Cranesbill | 100.00% | 100.00% | 100.00% |
| Sugar beet | 97.75% | 98.40% | 98.02% |

---

### efficientnet_v3

#### Architecture Details
- Total Parameters: 20,192,860

#### Cross-Validation Results

| Fold | Best Val Acc | Test Acc | Precision | Recall | F1-Score |
|------|-------------|----------|-----------|--------|----------|
| 1 | 97.04% | 97.33% | 97.41% | 97.33% | 97.34% |
| 2 | 97.59% | 96.33% | 96.47% | 96.33% | 96.32% |
| 3 | 96.67% | 95.67% | 95.73% | 95.67% | 95.66% |
| 4 | 96.85% | 97.67% | 97.76% | 97.67% | 97.65% |
| 5 | 97.41% | 96.67% | 96.78% | 96.67% | 96.66% |
| **Avg** | **97.11%** | **96.73% ± 0.71%** | **96.83%** | **96.73%** | **96.73%** |

#### Average Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Black-grass | 86.87% | 88.80% | 87.72% |
| Charlock | 100.00% | 100.00% | 100.00% |
| Cleavers | 100.00% | 96.00% | 97.96% |
| Common Chickweed | 96.15% | 100.00% | 98.04% |
| Common wheat | 92.64% | 100.00% | 96.17% |
| Fat Hen | 100.00% | 95.20% | 97.53% |
| Loose Silky-bent | 89.38% | 85.60% | 87.31% |
| Maize | 99.23% | 100.00% | 99.61% |
| Scentless Mayweed | 99.23% | 98.40% | 98.79% |
| Shepherds Purse | 98.46% | 99.20% | 98.81% |
| Small-flowered Cranesbill | 100.00% | 100.00% | 100.00% |
| Sugar beet | 100.00% | 97.60% | 98.78% |

---

### nasnet_large

#### Architecture Details
- Total Parameters: 84,768,546

#### Cross-Validation Results

| Fold | Best Val Acc | Test Acc | Precision | Recall | F1-Score |
|------|-------------|----------|-----------|--------|----------|
| 1 | 98.15% | 96.67% | 96.83% | 96.67% | 96.66% |
| 2 | 97.78% | 97.67% | 97.88% | 97.67% | 97.66% |
| 3 | 96.67% | 97.33% | 97.64% | 97.33% | 97.32% |
| 4 | 97.41% | 96.67% | 96.91% | 96.67% | 96.66% |
| 5 | 96.85% | 97.00% | 97.36% | 97.00% | 97.00% |
| **Avg** | **97.37%** | **97.07% ± 0.39%** | **97.32%** | **97.07%** | **97.06%** |

#### Average Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Black-grass | 84.27% | 98.40% | 90.77% |
| Charlock | 100.00% | 100.00% | 100.00% |
| Cleavers | 100.00% | 95.20% | 97.53% |
| Common Chickweed | 96.92% | 100.00% | 98.43% |
| Common wheat | 93.16% | 96.80% | 94.92% |
| Fat Hen | 100.00% | 96.00% | 97.96% |
| Loose Silky-bent | 98.14% | 81.60% | 89.08% |
| Maize | 96.92% | 100.00% | 98.43% |
| Scentless Mayweed | 99.23% | 99.20% | 99.20% |
| Shepherds Purse | 99.23% | 100.00% | 99.61% |
| Small-flowered Cranesbill | 100.00% | 100.00% | 100.00% |
| Sugar beet | 100.00% | 97.60% | 98.78% |

---

### vit_large_patch16

#### Architecture Details
- Total Parameters: 303,313,932

#### Cross-Validation Results

| Fold | Best Val Acc | Test Acc | Precision | Recall | F1-Score |
|------|-------------|----------|-----------|--------|----------|
| 1 | 21.67% | 25.33% | 29.37% | 25.33% | 22.38% |
| 2 | 70.74% | 63.67% | 63.59% | 63.67% | 62.64% |
| 3 | 64.07% | 61.00% | 62.49% | 61.00% | 59.78% |
| 4 | 81.11% | 77.67% | 78.23% | 77.67% | 77.60% |
| 5 | 70.19% | 64.00% | 64.86% | 64.00% | 62.17% |
| **Avg** | **61.56%** | **58.33% ± 17.50%** | **59.71%** | **58.33%** | **56.92%** |

#### Average Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Black-grass | 61.48% | 55.20% | 57.08% |
| Charlock | 62.25% | 79.20% | 69.24% |
| Cleavers | 63.19% | 74.40% | 68.25% |
| Common Chickweed | 56.97% | 59.20% | 52.02% |
| Common wheat | 70.60% | 75.20% | 72.60% |
| Fat Hen | 57.32% | 44.80% | 49.44% |
| Loose Silky-bent | 67.13% | 54.40% | 57.49% |
| Maize | 67.29% | 64.80% | 65.78% |
| Scentless Mayweed | 53.96% | 55.20% | 51.51% |
| Shepherds Purse | 35.10% | 32.00% | 32.83% |
| Small-flowered Cranesbill | 57.28% | 55.20% | 54.09% |
| Sugar beet | 63.93% | 50.40% | 52.66% |

---

### davit

#### Architecture Details
- Total Parameters: 86,941,708

#### Cross-Validation Results

| Fold | Best Val Acc | Test Acc | Precision | Recall | F1-Score |
|------|-------------|----------|-----------|--------|----------|
| 1 | 97.96% | 98.33% | 98.45% | 98.33% | 98.34% |
| 2 | 97.78% | 96.67% | 96.80% | 96.67% | 96.68% |
| 3 | 97.22% | 97.33% | 97.45% | 97.33% | 97.33% |
| 4 | 98.52% | 97.00% | 97.10% | 97.00% | 97.00% |
| 5 | 97.41% | 95.00% | 95.25% | 95.00% | 94.98% |
| **Avg** | **97.78%** | **96.87% ± 1.09%** | **97.01%** | **96.87%** | **96.87%** |

#### Average Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Black-grass | 88.34% | 91.20% | 89.59% |
| Charlock | 100.00% | 100.00% | 100.00% |
| Cleavers | 100.00% | 96.00% | 97.96% |
| Common Chickweed | 94.02% | 100.00% | 96.91% |
| Common wheat | 91.39% | 98.40% | 94.68% |
| Fat Hen | 100.00% | 92.80% | 96.24% |
| Loose Silky-bent | 93.48% | 88.80% | 91.03% |
| Maize | 99.23% | 100.00% | 99.61% |
| Scentless Mayweed | 100.00% | 97.60% | 98.78% |
| Shepherds Purse | 97.69% | 100.00% | 98.82% |
| Small-flowered Cranesbill | 100.00% | 100.00% | 100.00% |
| Sugar beet | 100.00% | 97.60% | 98.78% |

---

### swinv2

#### Architecture Details
- Total Parameters: 86,906,116

#### Cross-Validation Results

| Fold | Best Val Acc | Test Acc | Precision | Recall | F1-Score |
|------|-------------|----------|-----------|--------|----------|
| 1 | 98.15% | 97.67% | 97.91% | 97.67% | 97.66% |
| 2 | 97.96% | 98.33% | 98.47% | 98.33% | 98.33% |
| 3 | 96.67% | 97.67% | 97.77% | 97.67% | 97.66% |
| 4 | 96.67% | 96.67% | 96.79% | 96.67% | 96.67% |
| 5 | 97.04% | 96.67% | 96.86% | 96.67% | 96.67% |
| **Avg** | **97.30%** | **97.40% ± 0.65%** | **97.56%** | **97.40%** | **97.40%** |

#### Average Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Black-grass | 88.35% | 96.00% | 91.92% |
| Charlock | 100.00% | 100.00% | 100.00% |
| Cleavers | 100.00% | 96.00% | 97.96% |
| Common Chickweed | 94.73% | 100.00% | 97.29% |
| Common wheat | 93.28% | 99.20% | 96.14% |
| Fat Hen | 100.00% | 93.60% | 96.68% |
| Loose Silky-bent | 95.91% | 87.20% | 91.23% |
| Maize | 99.23% | 100.00% | 99.61% |
| Scentless Mayweed | 100.00% | 99.20% | 99.59% |
| Shepherds Purse | 99.23% | 100.00% | 99.61% |
| Small-flowered Cranesbill | 100.00% | 100.00% | 100.00% |
| Sugar beet | 100.00% | 97.60% | 98.78% |

---

### convnext_large

#### Architecture Details
- Total Parameters: 196,248,780

#### Cross-Validation Results

| Fold | Best Val Acc | Test Acc | Precision | Recall | F1-Score |
|------|-------------|----------|-----------|--------|----------|
| 1 | 97.78% | 98.33% | 98.47% | 98.33% | 98.33% |
| 2 | 97.59% | 97.00% | 97.14% | 97.00% | 96.99% |
| 3 | 97.59% | 97.67% | 97.69% | 97.67% | 97.67% |
| 4 | 97.78% | 96.67% | 96.82% | 96.67% | 96.66% |
| 5 | 97.96% | 97.00% | 97.16% | 97.00% | 97.00% |
| **Avg** | **97.74%** | **97.33% ± 0.60%** | **97.45%** | **97.33%** | **97.33%** |

#### Average Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Black-grass | 86.26% | 95.20% | 90.49% |
| Charlock | 100.00% | 100.00% | 100.00% |
| Cleavers | 100.00% | 96.00% | 97.96% |
| Common Chickweed | 97.69% | 100.00% | 98.82% |
| Common wheat | 96.18% | 98.40% | 97.24% |
| Fat Hen | 98.40% | 97.60% | 97.99% |
| Loose Silky-bent | 94.70% | 84.80% | 89.45% |
| Maize | 97.75% | 100.00% | 98.84% |
| Scentless Mayweed | 100.00% | 98.40% | 99.18% |
| Shepherds Purse | 98.46% | 100.00% | 99.22% |
| Small-flowered Cranesbill | 100.00% | 100.00% | 100.00% |
| Sugar beet | 100.00% | 97.60% | 98.78% |

---

### coatnet_3

#### Architecture Details
- Total Parameters: 163,654,872

#### Cross-Validation Results

| Fold | Best Val Acc | Test Acc | Precision | Recall | F1-Score |
|------|-------------|----------|-----------|--------|----------|
| 1 | 94.26% | 93.00% | 93.41% | 93.00% | 93.07% |
| 2 | 82.41% | 84.00% | 84.67% | 84.00% | 84.04% |
| 3 | 92.78% | 94.33% | 95.09% | 94.33% | 94.25% |
| 4 | 91.67% | 91.00% | 91.21% | 91.00% | 90.99% |
| 5 | 87.22% | 88.33% | 88.86% | 88.33% | 88.22% |
| **Avg** | **89.67%** | **90.13% ± 3.67%** | **90.65%** | **90.13%** | **90.11%** |

#### Average Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Black-grass | 84.76% | 72.80% | 77.74% |
| Charlock | 93.58% | 90.40% | 91.88% |
| Cleavers | 96.17% | 91.20% | 93.51% |
| Common Chickweed | 85.82% | 98.40% | 91.58% |
| Common wheat | 92.77% | 92.00% | 92.27% |
| Fat Hen | 92.65% | 88.80% | 90.64% |
| Loose Silky-bent | 76.98% | 87.20% | 81.51% |
| Maize | 97.69% | 100.00% | 98.82% |
| Scentless Mayweed | 91.75% | 92.80% | 92.13% |
| Shepherds Purse | 84.67% | 88.00% | 86.29% |
| Small-flowered Cranesbill | 93.66% | 90.40% | 91.91% |
| Sugar beet | 97.28% | 89.60% | 93.10% |

---

