## [torch 参数更多 ]torch.gather
### [torch.gather](https://pytorch.org/docs/stable/generated/torch.gather.html?highlight=gather#torch.gather)

```python
torch.gather(input,
             dim,
             index,
             *,
             sparse_grad=False,
             out=None)
```

### [paddle.take_along_axis](https://www.paddlepaddle.org.cn/documentation/docs/zh/api/paddle/take_along_axis_cn.html#take-along-axis)

```python
paddle.take_along_axis(arr,
                       indices,
                       axis)
```

其中 Pytorch 相比 Paddle 支持更多其他参数，具体如下：
### 参数映射
| PyTorch       | PaddlePaddle | 备注                                                   |
| ------------- | ------------ | ------------------------------------------------------ |
| input         | x            | 表示输入 Tensor ，仅参数名不一致。                                    |
| dim           | axis         | 用于指定 index 获取输入的维度，仅参数名不一致。                         |
| index         | indices      | 聚合元素的索引矩阵，维度和输入 (input) 的维度一致，仅参数名不一致。          |
| sparse_grad   | -            | 表示是否对梯度稀疏化，PaddlePaddle 无此参数，暂无转写方式。            |
| out           | -            | 表示目标 Tensor ， Paddle 无此参数，需要进行转写。               |


### 转写示例
#### out：指定输出
``` python
# PyTorch 写法：
t = torch.tensor([[1, 2], [3, 4]])
torch.gather(t, dim = 1, index = torch.tensor([[0, 0], [1, 0]]), out = y)

# Paddle 写法：
t = paddle.to_tensor([[1, 2], [3, 4]])
paddle.assign(paddle.take_along_axis(t, axis = 1, indices = [[0, 0], [1, 0]]), y)
```
