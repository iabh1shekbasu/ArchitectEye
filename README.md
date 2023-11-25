
# ArchitectEye: Multi-label Semantic Bridge Damage Segmentation

## Table of Contents
- [Introduction](#introduction)
- [File Descriptions](#file-descriptions)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Environment Setup](#environment-setup)
  - [File Structure](#file-structure)
  - [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [Contact](#contact)

## Introduction
This project presents a deep learning-based solution for automated bridge damage detection and segmentation, a critical challenge in maintaining the structural safety of global bridge infrastructure. Utilizing a Feature Pyramid Network (FPN) with an EfficientNet B4 backbone, pre-trained on ImageNet weights, our model excels in multi-label semantic segmentation. It is designed to work with the 'dacl10k: Dataset for Semantic Bridge Damage Segmentation', enabling the identification and classification of 19 different types of bridge damages. This model represents a significant advancement in the field of automated bridge damage detection. It not only demonstrates the potential of deep learning in structural safety assessments but also sets a new benchmark for future research endeavors. The model's ability to segment 19 different classes of damages is currently unmatched, showcasing our commitment to enhancing the safety and maintenance of both urban and rural bridge infrastructures. Our approach achieves state-of-the-art performance, particularly in terms of mean Intersection over Union (mIoU), further contributing to the field's development.

Our Model Weights can be found at https://mbzuaiac-my.sharepoint.com/:f:/g/personal/abhishek_basu_mbzuai_ac_ae/El8682rpwt5Ipi2tO5yPb38B1UJfZeFtUxKtIgxVl7lL6Q?e=Rf9yvB

## File Descriptions

- `create_pt_files.py`: Processes the 'dacl10k' dataset, resizing images and preparing them for training.
- `model.py`: Trains the deep learning model for bridge damage segmentation.

## Getting Started

### Prerequisites
```
### Download the dataset

| Data File                      | Download                        | sha256sum  | 
|--------------------------------|----------------------------------|-------------|
| `dacl10k_v2_devphase.zip`      | [[GigaMove]](https://gigamove.rwth-aachen.de/en/download/ae8278474b389aa9cc0ab6c406b7a466)¹ [[AWS]](https://dacl10k.s3.eu-central-1.amazonaws.com/dacl10k-challenge/dacl10k_v2_devphase.zip) | dcbcd5fb82699076a2c7f3a72492a9ef798870e0ca1f0c9399360f273ea95260 |

¹ Hosted at [RWTH Aachen University](https://gigamove.rwth-aachen.de/).

### Environment Setup

Create a virtual environment using Conda to manage dependencies:

```bash
conda create -n bridge-detection python=3.8
conda activate bridge-detection
pip install -r requirements.txt
```

### File Structure

Ensure your project directory follows this structure:

```
project/
├── annotations/
│   ├── train/ (n=6,935)
│   └── validation/ (n=975)
├── images/
│   ├── train/ (n=6,935)
│   └── validation/ (n=975)
├── create_pt_files.py
├── model.py
└── requirements.txt
```

### Installation

Clone the repository and navigate to the project directory:

```bash
git clone https://github.com/iabh1shekbasu/AI701_Course_Project.git 
cd AI701_Course_Project
```

## Usage

To use the scripts, follow these steps:

1. Process the 'dacl10k' dataset to generate .pt files, which significantly reduces training time. This step might take a while to run:

   ```bash
   python create_pt_files.py
   ```

2. Train the model (this step automatically handles data loading and preprocessing):

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

## Contact

For any inquiries or further information, please reach out to [abhishek.basu@mbzuai.ac.ae].
