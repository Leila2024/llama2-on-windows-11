# llama2-on-windows-11

This repository provides a comprehensive guide and necessary scripts to set up and run LLaMA2 (Large Language Model Architecture) on a Windows 11 machine using Anaconda. Follow the instructions below to get LLaMA2 up and running seamlessly.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
  - [Clone Repository](#clone-repository)
  - [Install Anaconda](#install-anaconda)
  - [Set Up Anaconda Environment](#set-up-anaconda-environment)
  - [Install Dependencies](#install-dependencies)
  - [Install PyTorch](#install-pytorch)
  - [Clone Text Generation Web UI Repository](#clone-text-generation-web-ui-repository)
  - [Change Directory](#change-directory)
  - [Install Python Modules](#install-python-modules)
  - [Start the Server](#start-the-server)
- [Access the Web UI](#access-the-web-ui)
- [Downloading LLaMA2 Model](#downloading-llama2-model)
- [Load the Model](#load-the-model)
- [Configure the Session](#configure-the-session)
- [Configure Parameters](#configure-parameters)
- [Test the Model](#test-the-model)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before starting, ensure you have the following:

- A Windows 11 PC with at least 16 GB of RAM.
- Administrative privileges to install software.
- Git installed on your machine. [Download Git](https://git-scm.com/downloads)
- Anaconda installed on your machine. [Download Anaconda](https://www.anaconda.com/products/distribution)
Method 1: Using nvcc Command
Open Command Prompt:

Check Python Version:

Type the following command and press Enter:
```bash
python --version
```
This will output the Python version information. For example:
```bash
Python 3.8.10
```

Check CUDA Version:

Type the following command and press Enter:

```bash
nvcc --version
```
This will output the CUDA version information. Look for a line similar to:

vbnet
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2022 NVIDIA Corporation
Built on Sun_Sep_22_19:32:54_PDT_2022
Cuda compilation tools, release 11.8, V11.8.89

## Installation

### Clone Repository

First, clone this repository to your local machine using Git.

```bash
git clone https://github.com/Leila2024/lama2.git
cd lama2
```

### Install Anaconda

Ensure Anaconda is installed on your machine. You can download it from the official [Anaconda website](https://www.anaconda.com/products/distribution).

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

### Clone Text Generation Web UI Repository

After installing PyTorch, clone the Text Generation Web UI repository.

```bash
git clone https://github.com/oobabooga/text-generation-webui.git
```

This command clones the repository into a new folder named `text-generation-webui`.

### Change Directory

Next, change the directory to the newly cloned folder.

```bash
cd text-generation-webui
```

### Install Python Modules

Inside the `text-generation-webui` folder, install all the required Python modules.

```bash
pip install -r requirements.txt
```

This command installs all the Python modules listed in the `requirements.txt` file. This process may take a few minutes.

### Start the Server

Now that all the necessary modules are installed, you can start the server with the following command:

```bash
python server.py
```

Once the server is running, you will see a local URL in your terminal.

## Access the Web UI

Copy the local URL from your terminal and paste it into your web browser. You should now see the Text Generation Web UI.

## Downloading LLaMA2 Model

### Choose a Model

I use the 70B Llama models which require a minimum of 32GB GPU RAM, but you can use the 13B or 7B models if your GPU can’t handle that.
7B Llama = TheBloke/Llama-2-7B-chat-GPTQ
13B Llama = TheBloke/Llama-2-13B-chat-GPTQ
70B Llama = TheBloke/Llama-2-70B-chat-GPTQ

### Download the Model

1. Go to the LLaMA 2 70b chat model on Hugging Face and copy the model URL. For example, "TheBloke/Llama-2-70B-chat-GPTQ".
2. Switch back to the Text Generation Web UI, go to the Model tab, and paste the partial URL into the “Download custom model” field.
3. Click “Download” to start the download. This process will take a significant amount of time due to the large file size of the model.

## Load the Model

Once the model is downloaded, click the blue “Reload” button at the top of the Model tab. Find the downloaded model in the list and click “Load”. Make sure to use the Transformers model loader for this process. This process may also take some time.

## Configure the Session

After loading the model, switch to the Session tab and select “Chat” from the Mode dropdown menu. Click “Apply and Restart” to apply the changes.

## Configure Parameters

Switch to the Parameters tab and max out the “New Tokens” field. Set the “Temperature” field to 0. You can adjust these settings later based on your needs.

## Test the Model

Finally, switch back to the Text Generation tab and test the model by typing something into the input field and clicking “Generate”.

And there you have it! You have successfully installed LLaMA 2 locally. Enjoy exploring the capabilities of this powerful AI model.

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
