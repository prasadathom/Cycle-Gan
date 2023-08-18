
# CycleGAN with Attention and Advanced Loss Functions

This project delves into the implementation and experimentation of CycleGAN, enhanced with attention mechanisms and a variety of loss functions.

## Description

CycleGAN is renowned for its capability in image-to-image translation without needing paired training data. This notebook seeks to refine the original CycleGAN by:
- Incorporating attention mechanisms to guide the generators.
- Experimenting with multiple loss functions including adversarial, style, perceptual, and cycle-consistency losses.

## Features

- **Custom Dataset Loader**: `ImageDataset` class for streamlined image-to-image translation tasks.
- **Visualization**: `show_tensor_images` function facilitates easy visualization of tensor images.
- **Attention Mechanisms**: Attention maps derived from discriminators guide the image translation process.
- **Advanced Loss Functions**: Incorporates adversarial loss, style loss, perceptual loss, and cycle-consistency loss to enhance image translation quality.
- **Loss Testing**: Validation of individual loss functions to ensure correctness.

## Libraries Used

- torch
- torchvision
- tqdm
- matplotlib
- PIL (Pillow)
- glob
- os
- random

## Usage

Ensure you have the necessary libraries installed. Refer to `requirements.txt` for the list of required libraries.

```python
# Load the dataset
transform = transforms.Compose([
    transforms.Resize(load_shape),
    transforms.RandomCrop(target_shape),
    transforms.RandomHorizontalFlip(),
    transforms.ToTensor(),
])
dataset = ImageDataset("../input/summer2winter-yosemite", transform=transform)
```

## Acknowledgments

- The `ImageDataset` class is inspired by [this CycleGAN dataset implementation](https://github.com/aitorzip/PyTorch-CycleGAN/blob/master/datasets.py).

---

*Note: This README provides an overview based on the notebook's content. For a detailed report, refer to the project report.*
