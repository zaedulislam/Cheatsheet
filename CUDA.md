# CUDA (Compute Unified Device Architecture)
* The architecture of the NVIDIA graphics processing unit (GPU), starting with its GeForce 8 chips. The CUDA programming interface (API) exposes the inherent parallel processing capabilities of the GPU to the developer and enables scientific and financial applications to be run on the graphics GPU chip rather than the CPU.
                                
#### How to check CUDA version on Ubuntu 20.04 step by step instructions
1. The first method is to check the version of the Nvidia CUDA Compiler `nvcc`. To do so execute: `nvcc --version`
2. Given that you have the [Nvidia driver installed on your Ubuntu 20.04](https://linuxconfig.org/how-to-install-the-nvidia-drivers-on-ubuntu-20-04-focal-fossa-linux) system, the following command will also reveal the CUDA version: `nvidia-smi`

---

## Error & Fix

1. 
```
RuntimeError: CUDA error: no kernel image is available for execution on the device
CUDA kernel errors might be asynchronously reported at some other API call,so the stacktrace below might be incorrect.
For debugging consider passing CUDA_LAUNCH_BLOCKING=1.
```

Apparently, it turned out that the error occured due to incompatible CUDA version. Following command solved it
```
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch
```

---

### Reference
1. [How to check CUDA version on Ubuntu 20.04 Focal Fossa Linux](https://linuxconfig.org/how-to-check-cuda-version-on-ubuntu-20-04-focal-fossa-linux)
2. [How to get CUDA Cores count on Linux](https://linuxconfig.org/how-to-get-cuda-cores-count-on-linux)
