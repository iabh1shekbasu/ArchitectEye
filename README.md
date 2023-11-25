# AI701 Course Project


# Project Title: Automated Bridge Damage Detection and Segmentation

## Table of Contents
- [Introduction](#introduction)
- [File Descriptions](#file-descriptions)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

This project presents a deep learning-based solution for automated bridge damage detection and segmentation, a critical challenge in maintaining the structural safety of global bridge infrastructure. Utilizing a Feature Pyramid Network (FPN) with an EfficientNet B4 backbone, pre-trained on ImageNet weights, our model excels in multi-label semantic segmentation. It is designed to work with the 'dacl10k: Dataset for Semantic Bridge Damage Segmentation', enabling the identification and classification of 19 different bridge damage classes. This achievement not only demonstrates significant progress in automated bridge damage detection but also lays a strong foundation for future research in structural safety and maintenance of both urban and rural bridge infrastructure. Our model sets a new benchmark with its state-of-the-art performance, particularly in terms of mean Intersection over Union (mIoU).

## File Descriptions

- `create_pt_files.py`: This script is essential for processing the 'dacl10k' dataset. It resizes images and prepares them for training, ensuring they are compatible with our deep learning model.
- `data_load.py`: This script manages the loading and preprocessing of the dataset. It is equipped to handle various data formats and structures, making it versatile for diverse image datasets.
- `model.py`: At the core of our project, this script defines and trains the deep learning model for bridge damage segmentation. It leverages advanced techniques and libraries to achieve superior performance.

## Getting Started

### Prerequisites

Before running the project, ensure you have the following installed:
- Python 3.6 or higher
- PyTorch
- torchvision
- numpy
- pandas
- segmentation_models_pytorch

Install them using pip:

```bash
pip install torch torchvision numpy pandas segmentation-models-pytorch
```

### Installation

Clone the repository and navigate to the project directory:

```bash
git clone https://github.com/yourusername/yourprojectname.git
cd yourprojectname
```

## Usage

To use the scripts, follow these steps:

1. Process the 'dacl10k' dataset:

   ```bash
   python create_pt_files.py
   ```

2. Load and preprocess the data:

   ```bash
   python data_load.py
   ```

3. Train the model:

   ```bash
   python model.py
   ```

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For any inquiries or further information, please reach out to [Your Email or Contact Information].
