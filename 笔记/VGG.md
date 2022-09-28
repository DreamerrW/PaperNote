## 文章：VERY DEEP CONVOLUTIONAL NETWORKS FOR LARGE-SCALE IMAGE RECOGNITION
### 摘要：
研究神经网络深度对大规模图像识别中准确率的影响，用3 × 3大小的卷积核来进行评估，实验表明神经网络深度在达到
16~19层时效果最好。

### Motivation
在AlexNet问世之后，许多学者对AlexNet的结构进行改进，希望得到更好的准确性，当时主要有两个方向，一个方向是
缩小卷积核和步长，一个方向是多尺度，作者选择了另一个方向：增加更多的卷积层来增加深度。

### FrameWork
>输入：固定尺寸为224 × 224的RGB图像 预处理：每个像素减去训练集中的RGB均值

规律：连续使用数个相同的填充为1、窗口形状为3×3的卷积层后接上一个步幅为2、窗口形状为2×2的最大池化层。卷积层
保持输入的高和宽不变，而池化层则对其减半。
池化层有5个，全连接层有三个，前两层是4096个通道，第三层是1000个通道，因为要实现1000个物体的分类。
所有隐含层都用Relu函数激活。最后一层是softmax层。

>VGG的结构图如下：

<img src="https://github.com/zju318010xxxx/PaperNote/blob/main/images/fig1.PNG" width="50%">

介绍一下区别：

·A：没啥特别的

A-L

>训练过程：

采用含动量的mini_batch SGD算法


