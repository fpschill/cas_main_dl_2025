# ZHAW CAS Machine Intelligence

# Module: Deep Learning (Fall Term 2025)


# Setup Instructions

## Versions required
	
	Python 3.10 		
	Tensorflow 2.16.1 	
	CUDA 12.3
	CUDNN 8.9.7
	scikit-image 0.24 		
	scikit-learn 1.5.2 		
	numpy 1.26.4 	

Official instructions to install Tensorflow: https://www.tensorflow.org/install/pip

## Automatic Environment Setup

### CPU

	conda env create -f env.yaml

This will create the conda environment "cas_main_dl" and install the required packages, as specified in the file "env.yaml" (CPU only).

### GPU 

**A. for labs XXX-XXX**

conda env create -f env_gpu.yaml

	# Create symbolic links to NVIDIA shared libraries:
	pushd $(dirname $(python -c 'print(__import__("tensorflow").__file__)'))
	ln -svf ../nvidia/*/lib/*.so* .
	popd

For detailed installation instructions, see https://www.tensorflow.org/install/pip

**B. for Labs XXX,XXX:**

	conda env create -f env_gpu2.yaml

### Manual Setup

	# create and activate env
    conda create -n cas_main_dl python=3.10
    conda activate cas_main_dl

    # Install Tensorflow
	# Either: GPU
	pip install tensorflow[and-cuda]==2.16.1
	# Or: CPU 
	pip install tensorflow==2.16.1

	# install other packages (check versions above)
	pip install wget notebook matplotlib pandas tqdm ipywidgets scikit-learn scikit-image

## Run directly in Colab

If you have forked the repository, you can run a notebook directly in Google Colab by using a link like this:

https://colab.research.google.com/github/(YOUR_GITHUB_ID)/cas_main_dl_2024/blob/master/01_mnist.ipynb

## Prepare Tensorflow with GPU on WSL2 (Windows Subsystem for Linux)

For Windows (in particular when using a GPU), it is strongly recommended to install and use Tensorflow within WSL2 (Windows Subsystem for Linux). Without GPU (CPU only), you can still also use native Windows if you want.

	
Install WSL2, see https://docs.microsoft.com/windows/wsl/install

