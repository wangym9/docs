## [ torch 参数更多 ]torch.cosh
### [torch.cosh](https://pytorch.org/docs/stable/generated/torch.cosh.html#torch.cosh)

```python
torch.cosh(input,
           *,
           out=None)
```

### [paddle.cosh](https://www.paddlepaddle.org.cn/documentation/docs/zh/api/paddle/cosh_cn.html#cosh)

```python
paddle.cosh(x,
            name=None)
```

其中 Pytorch 相比 Paddle 支持更多其他参数，具体如下：
### 参数映射
| PyTorch       | PaddlePaddle | 备注                                                   |
| ------------- | ------------ | ------------------------------------------------------ |
| input  |  x  | 表示输入的 Tensor，仅参数名不一致。  |
|  out   |  -  | 表示输出的 Tensor，Paddle 无此参数，需要进行转写。    |


### 转写示例
#### out：指定输出
```python
# Pytorch 写法
torch.cosh(torch.tensor([0.1632, 1.1835]), out=y)

# Paddle 写法
paddle.assign(paddle.cosh(paddle.to_tensor([0.1632, 1.1835])), y)
```
