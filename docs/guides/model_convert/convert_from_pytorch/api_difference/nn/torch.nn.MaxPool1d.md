## [torch 参数更多 ]torch.nn.MaxPool1d
### [torch.nn.MaxPool1d](https://pytorch.org/docs/stable/generated/torch.nn.MaxPool1d.html?highlight=maxpool1d#torch.nn.MaxPool1d)

```python
torch.nn.MaxPool1d(kernel_size,
                   stride=None,
                   padding=0,
                   dilation=1,
                   return_indices=False,
                   ceil_mode=False)
```

### [paddle.nn.MaxPool1D](https://www.paddlepaddle.org.cn/documentation/docs/zh/api/paddle/nn/MaxPool1D_cn.html#maxpool1d)

```python
paddle.nn.MaxPool1D(kernel_size,
                    stride=None,
                    padding=0,
                    return_mask=False,
                    ceil_mode=False,
                    name=None)
```

其中 Pytorch 相比 Paddle 支持更多其他参数，具体如下：
### 参数映射
| PyTorch       | PaddlePaddle | 备注                                                   |
| ------------- | ------------ | ------------------------------------------------------ |
| kernel_size          | kernel_size            | 表示池化核大小。                           |
| stride          | stride            | 表示池化核步长。                           |
| padding          | padding            | 表示填充大小。                           |
| dilation      | -            | 设置空洞池化的大小，PaddlePaddle 无此参数，暂无转写方式。               |
| return_indices | return_mask  | 是否返回最大值的索引，仅参数名不一致。                                  |
| ceil_mode | ceil_mode  | 表示是否用 ceil 函数计算输出的 height 和 width 。                                  |
