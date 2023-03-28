# Ubuntu

Nvidia Install Steps
- Install a Ubuntu LTS version
- From my experience, it's better to select the Install Ubuntu (Safe Graphics) option
- Check the Install third-party software for graphics and Wi-Fi hardawre and media formats
- The above two opions is installing suitable Nvidia drivers during installation
- Otherwise, 
- First install the Nvidia display driver from [here](https://www.nvidia.com/download/index.aspx) (Fill the options with your GPU configuration)
- To chck weather the the driver installed or not. Check `nvidia-smi`.
- Now download the [CUDA Toolkit](https://developer.nvidia.com/cuda-toolkit-archive) that compatiable with pytorch or tensorflow
- Install [Anaconda](https://www.anaconda.com/products/distribution)
- Next check the CUDA version support [Pytorch](https://pytorch.org/get-started/locally/) or [Tensorflow](https://www.tensorflow.org/install/pip)
- Check the nvcc version `nvcc --version`



# References
- https://github.com/Shakib-IO/scribble/blob/main/Linux.md
