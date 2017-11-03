# 3D Reconstruction
###### 许卓尔

## Mobile Phone and Cloud - a Dream Team for 3D Reconstruction

> 主要讲的是以服务器/云端方式对移动端完成3D重建的应用程序的框架方案，有两大特色；
> 这篇比较水，只是提出一种框架而已，而且框架说的还不怎么具体；

SFM(Structure-from-motion pipelines)方法：
由于手机的性能、电量问题，要实现移动端的3D重建功能，前端、后端按如下分配：
- frontend 3D模型显示   手机
- backend 3D重建、生成模型 服务器/云端

动态加载平衡：根据CPU温度、带宽和电量，在客户端对3D显示运算做了动态平衡；
协作地形建模：用户可以看到之前的模型，引导用户拍照；

#### 使用方法
- offline SfM
- SLAM(Simultainous Localization and Mapping) 同步定位功能

#### 具体流程

可见3/8的图片；
- 动态平衡加载：图像获得得到视频流，通过图像追踪获得关键帧；
- 任务委托：进行重建、定位、辨别，得到服务器端会话模型；
- 先验知识：通过SLAM得到曾经建立的模型，进行模型融合、循环闭包，协作建模，返回用户；

#### 框架特色

分为global model和session model，通过SLAM技术将session model增强到global model中获得更好的3D重建效果，并且能看到用户看不到的部分（其他用户拍下来的）；




## Stereo Reconstruction using top-down cues

> 统一化自底向上、自顶向下的3D重建方法；
> 自底向上的重建方法，通过匹配、归并子单元 —— 等同于人类视觉系统；
> 这篇蛮好的，两种方法都有具体解释和实现；
>

#### 自底向上的重建方法

#### 自顶向下的重建方法

#### 联合框架


## Divide and Conquer: A hierarchical approach to large-scale structure-from-motion

> SFM方法，主要针对数据量特别大（1000张图像）的SFM的解决方法——分而治之；


## Shape From Motion

#### 提取Track Featrures（轨道特征）

检测好的特征，通过SIFT（尺度不变特征变换）方法匹配 ；
KLT Tracking；Kanade-Lucas-Tomasi方法进行轨道特征跟踪；

#### 建立运动模型
简化投影

#### 精炼模型

#### 恢复表面信息 


