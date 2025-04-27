# ECG_back
Based on Conductive Fiber and Deep Learning Electrocardiogram (ECG) Monitoring System_Back

Core value:
1.最耗时间的：找合适的库，编码；

2.SMTP开始加了个延迟发送，但是可能由于网络原因什么的，一直发送不了，最终去掉延迟成功解决。

3.实时渲染：模拟真实心电数据，500hz高频数据，容易导致后台和网络崩溃，后采用缓存机制缓存高频数据进行展示，前端页面更新时间1s  

4.诊断模型CNN+LSTM+通道注意力太复杂导致过拟合，减少卷积层数，测试准确率上升；

5.亟待解决的问题：由于心电异常类型N,V,S 数据趋势差别小，会误将N判断为V

Core value:
5.搭建EMQX服务器和远程数据库，配置环境是非常麻烦且复杂的一件事，需要耐心

6.TensorFlow 深度学习框架：最开始用的CPU训练，非常非常慢；windows不支持最新tensorflow，[GPU](https://so.csdn.net/so/search?q=GPU&spm=1001.2101.3001.7020) 支持仅适用于 2.10 或更早版本，从 TF 2.11 开始，Windows 不支持 CUDA 构建。建议重新配置一个conda环境，否则降级python会出现很多新的其他组件不匹配问题）下载相应的cuda和cudnn 我的是cuda11.8 cudnn8.6够用
