# llama2-on-windows-11

This repository provides a comprehensive guide and necessary scripts to set up and run LLaMA2 (Large Language Model Architecture) on a Windows 11 machine using Anaconda. You can follow the instructions below to get LLaMA2 up and running smoothly.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
  - [Clone Repository](#clone-repository)
  - [Install Anaconda](#install-anaconda)
  - [Set Up Anaconda Environment](#set-up-anaconda-environment)
  - [Install Dependencies](#install-dependencies)
- [Downloading LLaMA2 Model](#downloading-llama2-model)
- [Running LLaMA2](#running-llama2)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before starting, ensure you have the following:

- A Windows 11 PC with at least 16 GB of RAM.
- Administrative privileges to install software.
- Git installed on your machine. [Download Git](https://git-scm.com/downloads)
- Anaconda installed on your machine. [Download Anaconda](https://www.anaconda.com/products/distribution)

## Installation

### Clone Repository

First, clone the repository to your local machine using Git.

```bash
git clone https://github.com/Leila2024/llama2-on-windows-11.git
cd llama2-on-windows-11
```

### Install Anaconda

Please make sure Anaconda is installed on your machine. You can download it from the official [Anaconda website](https://www.anaconda.com/products/distribution).

### Set Up Anaconda Environment

Create a new Anaconda environment for LLaMA2.

```bash
conda create --name llama2 python=3.8
```

Activate the environment.

```bash
conda activate llama2
```
### Install PyTorch

Go to [PyTorch Get Started Locally](https://pytorch.org/get-started/locally/) and create your PC PyTorch installation command. For a typical Windows setup, you can use the following command:

```bash
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
```

### Install Dependencies

Install the required Python packages.

```bash
pip install -r requirements.txt
```

## Downloading LLaMA2 Model

You need to download the LLaMA2 model weights separately. Follow these steps:

1. Visit the official [LLaMA2 Model Page](https://lachieslifestyle.com/2023/07/29/how-to-install-llama-2/) and download the model weights.
2. Place the downloaded weights in the `models/llama2` directory within this repository.

## Running LLaMA2

After setting up the environment and downloading the model, you can run LLaMA2 using the provided scripts.

```bash
python run_llama2.py
```

This script will initialize the model and run it, allowing you to interact with it.

## Troubleshooting

If you encounter any issues, refer to the following common problems and solutions:

- **Conda Environment Activation Issue:** Ensure you are using the correct command for your shell (Command Prompt or PowerShell).
- **Missing Dependencies:** Run `pip install -r requirements.txt` again to ensure all dependencies are installed.
- **Model Not Found:** Verify that the model weights are placed in the correct directory.

## Contributing

We welcome contributions! Please read our [CONTRIBUTING](CONTRIBUTING.md) guidelines before making any contributions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to reach out if you have any questions or issues. Happy modeling!
