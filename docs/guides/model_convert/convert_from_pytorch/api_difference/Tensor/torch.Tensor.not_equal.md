## [ 参数不一致 ] torch.Tensor.not_equal
### [torch.Tensor.not_equal](https://pytorch.org/docs/stable/generated/torch.Tensor.not_equal.html)

```python
torch.Tensor.not_equal(other)
```

### [paddle.Tensor.not_equal](https://www.paddlepaddle.org.cn/documentation/docs/zh/api/paddle/Tensor_cn.html#not-equal-y-name-none)

```python
paddle.Tensor.not_equal(y)
```

其中，Paddle 与 PyTorch 的 `other` 参数所支持类型不一致，具体如下：

### 参数映射
| PyTorch       | PaddlePaddle | 备注                                             |
| ------------- | ------------ | ----------------------------------------------- |
| other         | y            | 比较的元素，PyTorch 支持 Tensor 和 Python Number，Paddle 仅支持 Tensor，需要进行转写。                       |

### 转写示例
#### other：比较的元素
```python
# PyTorch 写法
y = x.not_equal(other=2)

# Paddle 写法
y = x.not_equal(y=paddle.to_tensor(2))
```
