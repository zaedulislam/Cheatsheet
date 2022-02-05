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

- [CONV2D](https://pytorch.org/docs/stable/generated/torch.nn.Conv2d.html): Applies a 2D convolution over an input signal composed of several input planes.
```
torch.nn.Conv2d(in_channels, out_channels, kernel_size, stride=1, padding=0, dilation=1, groups=1, bias=True, padding_mode='zeros', device=None, dtype=None)
```
- [LINEAR](https://pytorch.org/docs/stable/generated/torch.nn.Linear.html)
```
torch.nn.Linear(in_features, out_features, bias=True, device=None, dtype=None)
```

###### Example
```
>>> m = nn.Linear(20, 30)
>>> input = torch.randn(128, 20)
>>> output = m(input)
>>> print(output.size())
torch.Size([128, 30])
```

---

###### Version Check

* `import torch`
* `print(torch.__version__)`

---
