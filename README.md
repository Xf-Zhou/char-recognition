# char-recognition 街景字符识别
## 代码文件
- input文件夹
   用来存放数据集，从天池官网下载
- output文件夹
   保存之前训练好的模型和要提交的测试集标签文件
- code
   - character recognition.ipynb
   利用预训练模型ResNet18搭建神经网络模型，去除最后一个fc layer,并联5个fc layer用于分类。
   

## 实验总结
这次实践是天池上的一个字符识别比赛mchar，数据集使用的是Google街景图像门牌号数据集SVHM，任务是识别不定长街景门牌字符。

解决这个问题的思路可以有多种。一是当作图像分类问题，首先固定字符的长度，然后在CNN后添加多个全连接分支进行多字符分类，按顺序把多个分支的结果连接，作为最终的结果输出。二是当作目标检测问题，首先检测出每张图片中的多个字符，然后按顺序把字符连接起来，作为最终的结果输出。
这个比赛给了一个baseline基础代码，格式是jupyter notebook。最后我的提交结果如下：

![image](https://github.com/Xf-Zhou/char-recognition/images/20200913235608.png)
