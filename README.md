# UNetRecon: Anomaly Detection with UNet Feature Reconstruction

This repository contains an implementation of an anomaly detection model that utilizes a UNet architecture for feature reconstruction and EfficientNet-B4 for feature extraction.

## Overview

The UNetRecon model is designed for unsupervised anomaly detection in images. It works by:

1. Extracting features from input images using a pre-trained EfficientNet-B4 model.
2. Reconstructing these features using a UNet architecture.
3. Comparing the reconstructed features to the original features to detect anomalies.

## Repository Structure

- `unet_recon.py`: Main model implementation and training script.
- `custom_dataset.py`: Custom dataset loader for training and evaluation.
- `utils.py`: Utility functions for performance metrics and visualization.
- `config.yaml`: Configuration file for model and training parameters.

## Requirements

- Python 3.7+
- PyTorch
- torchvision
- numpy
- matplotlib
- scikit-learn
- PyYAML
- tqdm

## Installation

Clone this repository and install the required packages:

```bash
git clone https://github.com/yourusername/UNetRecon.git
cd UNetRecon
pip install -r requirements.txt
```

## Usage

1. Prepare your dataset and update the `config.yaml` file with the correct paths and parameters.

2. Train the model:

```bash
python unet_recon.py config.yaml
```

3. For evaluation, set `eval_mode = True` in the `create_and_run_model` function call in `unet_recon.py`.

## Model Architecture

- Feature Extractor: EfficientNet-B4 (pre-trained on ImageNet)
- Feature Reconstructor: UNet

## Configuration

You can modify the model and training parameters in `config.yaml`. Key configurations include:

- Model path
- Number of epochs
- Learning rate
- Weight decay
- Feature extractor choice
- Dataset paths and parameters

## Performance

The model's performance is evaluated using:

- Area Under the Receiver Operating Characteristic (AUROC) curve
- Accuracy
- Precision, Recall, and F1-score (when verbose mode is enabled)

## License

[Specify your license here]

## Contributing

[Specify your contribution guidelines here]

## Contact

[Your contact information or link to issues page]