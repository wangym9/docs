## [ torch 参数更多 ]torch.negative

### [torch.negative](https://pytorch.org/docs/stable/generated/torch.negative.html?highlight=torch+negative#torch.negative)

```python
torch.negative(input, *, out=None)
```

### [paddle.neg](https://www.paddlepaddle.org.cn/documentation/docs/zh/api/paddle/neg_cn.html)

```python
paddle.neg(x, name=None)
```

Pytorch 相比 Paddle 支持更多其他参数，具体如下：

### 参数映射

| PyTorch                             | PaddlePaddle | 备注                                                                    |
| ----------------------------------- | ------------ | ----------------------------------------------------------------------- |
| input     | x           | 表示输入的 Tensor ，仅参数名不一致。                         |
| out           | -      | 表示输出的 Tensor ， Paddle 无此参数，需要进行转写。         |

###  转写示例
#### out：指定输出
```python
# Pytorch 写法
torch.negative(x ,out = y)

# Paddle 写法
paddle.assign(paddle.neg(x), y)
```
