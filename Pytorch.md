# Pytorch

## Error & Solution

### 1. Error: [OSError: undefined symbol: free_gemm_select, version libcublasLt.so.11](https://discuss.pytorch.org/t/oserror-undefined-symbol-free-gemm-select-version-libcublaslt-so-11/113487)

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

###### Version Check

* `import torch`
* `print(torch.__version__)`

---
