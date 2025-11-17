# ZHAW CAS Machine Intelligence

# Module: Deep Learning (Fall Term 2025)


# Local Setup

    # Versions
	
	Python 3.10 		
	Tensorflow 2.16.1 	
	CUDA 12.3
	CUDNN 8.9.7
	skimage 0.24 		
	sklearn 1.5.2 		
	numpy 1.26.4 	

Official instructions to install Tensorflow: https://www.tensorflow.org/install/pip
	
	

# Setup Environment

## 1. Create env

    conda create -n cas_main_dl python=3.10
    conda activate cas_main_dl

## 2. Install Tensorflow

	# Either: GPU
	pip install tensorflow[and-cuda]==2.16.1
	# Or: CPU 
	pip install tensorflow==2.16.1

## 3. Other packages

	pip install wget notebook matplotlib pandas tqdm ipywidgets scikit-learn scikit-image
	
	
For detailed installation instructions, see https://www.tensorflow.org/install/pip


# Run directly in Colab

If you have forked the repository, you can run a notebook directly in Google Colab by using a link like this:

https://colab.research.google.com/github/(YOUR_GITHUB_ID)/cas_main_dl_2024/blob/master/01_mnist.ipynb

# Prepare Tensorflow with GPU on WSL2 (Windows Subsystem for Linux)

For Windows (in particular when using a GPU), it is strongly recommended to install and use Tensorflow within WSL2 (Windows Subsystem for Linux). Without GPU (CPU only), you can still also use native Windows if you want.

	
Install WSL2, see https://docs.microsoft.com/windows/wsl/install

