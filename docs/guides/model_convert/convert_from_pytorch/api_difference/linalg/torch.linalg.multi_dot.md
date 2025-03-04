## [ torch 参数更多 ]torch.linalg.multi_dot

### [torch.linalg.multi_dot](https://pytorch.org/docs/stable/generated/torch.linalg.multi_dot.html?highlight=torch+linalg+multi_dot#torch.linalg.multi_dot)

```python
torch.linalg.multi_dot(tensors,
                       out=None)
```

### [paddle.linalg.multi_dot](https://www.paddlepaddle.org.cn/documentation/docs/zh/api/paddle/linalg/multi_dot_cn.html)

```python
paddle.linalg.multi_dot(x,
                       name=None)
```

Pytorch 相比 Paddle 支持更多其他参数，具体如下：
### 参数映射
| PyTorch       | PaddlePaddle | 备注                                                   |
| ------------- | ------------ | ------------------------------------------------------ |
| tensors | x         | 表示输入的一个 tensor 列表 ，仅参数名不一致。                    |
| out       | -       | 表示输出的 Tensor ， Paddle 无此参数，需要进行转写。 |

### 转写示例

#### out：指定输出

```python
# Pytorch 写法
torch.linalg.multi_dot(x, out=y)

# Paddle 写法
paddle.assign(paddle.linalg.multi_dot(x), y)
```
