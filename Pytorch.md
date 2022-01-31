# Pytorch


## Python API
### torch
#### Commonly Used
- [TORCH.ZEROS](https://pytorch.org/docs/stable/generated/torch.zeros.html): Returns a tensor filled with the scalar value 0, with the shape defined by the variable argument `size`.

```
torch.zeros(*size, *, out=None, dtype=None, layout=torch.strided, device=None, requires_grad=False) → Tensor
```

###### Example
```
>>> torch.zeros(2, 3)
tensor([[ 0.,  0.,  0.],
        [ 0.,  0.,  0.]])

>>> torch.zeros(5)
tensor([ 0.,  0.,  0.,  0.,  0.])
```
- [TORCH.ONES_LIKE](https://pytorch.org/docs/stable/generated/torch.ones_like.html#torch-ones-like): Returns a tensor filled with the scalar value 1, with the same size as `input`.

```
torch.ones_like(input, *, dtype=None, layout=None, device=None, requires_grad=False, memory_format=torch.preserve_format) → Tensor
```

###### Example
```
>>> input = torch.empty(2, 3)
>>> torch.ones_like(input)
tensor([[ 1.,  1.,  1.],
        [ 1.,  1.,  1.]])
```

- [TORCH.MATMUL](https://pytorch.org/docs/stable/generated/torch.matmul.html#torch.matmul): Matrix product of two tensors.
```
torch.matmul(input, other, *, out=None) → Tensor
```

---

###### Version Check

* `import torch`
* `print(torch.__version__)`

---
