# CUDA (Compute Unified Device Architecture)
* The architecture of the NVIDIA graphics processing unit (GPU), starting with its GeForce 8 chips. The CUDA programming interface (API) exposes the inherent parallel processing capabilities of the GPU to the developer and enables scientific and financial applications to be run on the graphics GPU chip rather than the CPU.
                                
#### How to check CUDA version on Ubuntu 20.04 step by step instructions
1. The first method is to check the version of the Nvidia CUDA Compiler `nvcc`. To do so execute: `nvcc --version`
2. Given that you have the [Nvidia driver installed on your Ubuntu 20.04](https://linuxconfig.org/how-to-install-the-nvidia-drivers-on-ubuntu-20-04-focal-fossa-linux) system, the following command will also reveal the CUDA version: `nvidia-smi`

---

## Error & Solution

### 1. Error
```
RuntimeError: CUDA error: no kernel image is available for execution on the device
CUDA kernel errors might be asynchronously reported at some other API call,so the stacktrace below might be incorrect.
For debugging consider passing CUDA_LAUNCH_BLOCKING=1.
```

### Solution

Apparently, it turned out that the error occured due to incompatible CUDA version. Following command solved it
```
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch
```

### 2. Error
```
pip install torch==1.7.0+cu110 torchvision==0.8.0+cu110 torchaudio==0.7.0 -f https://download.pytorch.org/whl/torch_stable.html
Looking in links: https://download.pytorch.org/whl/torch_stable.html
Collecting torch==1.7.0+cu110
  Using cached https://download.pytorch.org/whl/cu110/torch-1.7.0%2Bcu110-cp38-cp38-linux_x86_64.whl (1137.1 MB)

ERROR: Could not find a version that satisfies the requirement torchvision==0.8.0+cu110 (from versions: 0.1.6, 0.1.7, 0.1.8, 0.1.9, 0.2.0, 0.2.1, 0.2.2, 0.2.2.post2, 0.2.2.post3, 0.5.0, 0.5.0+cpu, 0.5.0+cu100, 0.5.0+cu92, 0.6.0, 0.6.0+cpu, 0.6.0+cu101, 0.6.0+cu92, 0.6.1, 0.6.1+cpu, 0.6.1+cu101, 0.6.1+cu92, 0.7.0, 0.7.0+cpu, 0.7.0+cu101, 0.7.0+cu92, 0.8.0, 0.8.1, 0.8.1+cpu, 0.8.1+cu101, 0.8.1+cu110, 0.8.1+cu92, 0.8.2, 0.8.2+cpu, 0.8.2+cu101, 0.8.2+cu110, 0.8.2+cu92, 0.9.0, 0.9.0+cpu, 0.9.0+cu101, 0.9.0+cu111, 0.9.1, 0.9.1+cpu, 0.9.1+cu101, 0.9.1+cu102, 0.9.1+cu111, 0.10.0, 0.10.0+cpu, 0.10.0+cu102, 0.10.0+cu111, 0.10.0+rocm4.1, 0.10.0+rocm4.2, 0.10.1, 0.10.1+cpu, 0.10.1+cu102, 0.10.1+cu111, 0.10.1+rocm4.1, 0.10.1+rocm4.2, 0.11.0, 0.11.0+cpu, 0.11.0+cu102, 0.11.0+cu111, 0.11.0+cu113, 0.11.0+rocm4.1, 0.11.0+rocm4.2, 0.11.1, 0.11.1+cpu, 0.11.1+cu102, 0.11.1+cu111, 0.11.1+cu113, 0.11.1+rocm4.1, 0.11.1+rocm4.2, 0.11.2, 0.11.2+cpu, 0.11.2+cu102, 0.11.2+cu111, 0.11.2+cu113, 0.11.2+rocm4.1, 0.11.2+rocm4.2, 0.11.3, 0.11.3+cpu, 0.11.3+cu102, 0.11.3+cu111, 0.11.3+cu113, 0.11.3+rocm4.1, 0.11.3+rocm4.2)

ERROR: No matching distribution found for torchvision==0.8.0+cu110
```

### Solution
Following this link: https://github.com/pytorch/vision/issues/2912, the above problem is solved by replacing with `torchvision==0.8.1`
```
pip install torch==1.7.0+cu110 torchvision==0.8.1+cu110 torchaudio===0.7.0 -f https://download.pytorch.org/whl/torch_stable.html
```

### 3. Error
Enable anomaly detection to find the operation that failed to compute its gradient, with torch.autograd.set_detect_anomaly(True)

### Solution
- It was due to imcompatible Pytorch version

---

### Reference
1. [How to check CUDA version on Ubuntu 20.04 Focal Fossa Linux](https://linuxconfig.org/how-to-check-cuda-version-on-ubuntu-20-04-focal-fossa-linux)
2. [How to get CUDA Cores count on Linux](https://linuxconfig.org/how-to-get-cuda-cores-count-on-linux)
3. https://discuss.pytorch.org/t/need-help-trouble-with-cuda-capability-sm-86/120235
