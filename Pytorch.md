# Pytorch

###### Version Check

* `import torch`
* `print(torch.__version__)`
---


## Error & Solution

### 1. Error: [OSError: undefined symbol: free_gemm_select, version libcublasLt.so.11](https://discuss.pytorch.org/t/oserror-undefined-symbol-free-gemm-select-version-libcublaslt-so-11/113487)
```
Traceback (most recent call last):
  File "main_graph.py", line 12, in <module>
    import torch
  File "/home/zayed/anaconda3/envs/spatial_temporal_gcn/lib/python3.8/site-packages/torch/__init__.py", line 189, in <module>
    _load_global_deps()
  File "/home/zayed/anaconda3/envs/spatial_temporal_gcn/lib/python3.8/site-packages/torch/__init__.py", line 142, in _load_global_deps
    ctypes.CDLL(lib_path, mode=ctypes.RTLD_GLOBAL)
  File "/home/zayed/anaconda3/envs/spatial_temporal_gcn/lib/python3.8/ctypes/__init__.py", line 373, in __init__
    self._handle = _dlopen(self._name, mode)
OSError: /home/zayed/anaconda3/envs/spatial_temporal_gcn/lib/python3.8/site-packages/torch/lib/../../../../libcublas.so.11: undefined symbol: free_gemm_select, version libcublasLt.so.11
```

### [Solution](https://github.com/pytorch/pytorch/issues/51080#issuecomment-787133939)
This should be resolved now that we’re no longer producing CUDA 11.0 binaries and now only produce CUDA 11.1 binaries.

For nightlies use:
```
conda install -y -c conda-forge -c pytorch-nightly pytorch cudatoolkit=11.1
```

For stable binaries you’ll have to wait until our release of v1.8.0 but after that you’ll be able to use:
```
conda install -y -c conda-forge -c pytorch pytorch cudatoolkit=11.1
```

If you’d like to test that experience right now you can use:
```
conda install -y -c conda-forge -c pytorch-test pytorch cudatoolkit=11.1
```
### 2. Error 
```
Traceback (most recent call last):
  File "/home/zayed/Research/Spatial-temporal GCN/main_graph.py", line 132, in <module>
    mean_error = train(opt, actions, train_dataloader, model, criterion, optimizer_all)
  File "/home/zayed/Research/Spatial-temporal GCN/train_graph_time.py", line 185, in train
    return step('train',  opt,actions,train_loader, model, criterion, optimizer)
  File "/home/zayed/Research/Spatial-temporal GCN/train_graph_time.py", line 146, in step
    loss.backward()
  File "/home/zayed/anaconda3/envs/spatial_temporal_gcn/lib/python3.10/site-packages/torch/_tensor.py", line 363, in backward
    torch.autograd.backward(self, gradient, retain_graph, create_graph, inputs=inputs)
  File "/home/zayed/anaconda3/envs/spatial_temporal_gcn/lib/python3.10/site-packages/torch/autograd/__init__.py", line 173, in backward
    Variable._execution_engine.run_backward(  # Calls into the C++ engine to run the backward pass
RuntimeError: one of the variables needed for gradient computation has been modified by an inplace operation: [torch.cuda.FloatTensor [256, 1024]], which is output 0 of ReluBackward0, is at version 1; expected version 0 instead. Hint: enable anomaly detection to find the operation that failed to compute its gradient, with torch.autograd.set_detect_anomaly(True).
```
### Solution
It could be due to the incompatible version PyTorch and CUDA version. Following installation solved,
```
conda install pytorch==1.8.0 torchvision==0.9.0 torchaudio==0.8.0 cudatoolkit=11.1 -c pytorch -c conda-forge
```

