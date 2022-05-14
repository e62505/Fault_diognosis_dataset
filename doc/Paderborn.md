# 德国 帕德博恩大学 Bearing DataCenter

## 1.简介
数据下载链接：https://mb.uni-paderborn.de/kat/forschung/datacenter/bearing-datacenter/
研究所和KAt-DataCenter链接的名称：Christian Lessmeier等，KAt-DataCenter：mb.uni-paderborn.de/kat/datacenter，


## 2.试验条件

试验台由(1) .电动机, (2).测力矩轴, (3).滚动轴承测试模块, (4).飞轮和(5).负载电机组成，如图1所示。将不同损伤类型的球轴承安装在轴承测试模块中，生成实验数据。滚动轴承模块使测试轴承在恒定径向载荷下运转，在每次试验前可调整至10 kN。

电机(1)是一个425 W永磁同步电动机, 其额定转矩T = 1.35 Nm, 额定转速n = 3000 rpm,标称电流I = 2.3 A。它由一个频率逆变器(KEB Combivert 07F5E 1D-2B0A)操作，开关频率为16 kHz。采用LEM CKSR 15- np型电流传感器测量电机相电流，测量精度为IPN = 15 a的0.8%。然后MCS经过25khz低通滤波器滤波，将模拟信号转换为采样率为64khz的数字信号。

## 3.数据集概述

​      PU数据集由Christian Lessmeier 等人提供，用于数据驱动的轴承故障诊断。数据集所使用的轴承包括人工加工而成的故障轴承、加速寿命测试造成的真实故障轴承以及健康轴承。轴承的型号为6203深沟球轴承。通过实验以64kHz的高频率同步采集了轴承在如表1所示的四种不同转速以及负载下的电机电流信号和振动信号。根据Christian Lessmeier等人的实验基于振动信号的分类比基于电机电流信号的分类具有更高的分类精度。
数据集共包含26种轴承损伤状态和6种健康状态的数据、以高频率同步采集了电机电流信号和振动信号。每种类别的轴承都在如下表所示的四种转速和荷载不同的工况下进行了数据采集。

### Table 6. Operating parameters

| No. | Rotational speed [rpm] | Load Torque [Nm] | Radial force [N] | Name of  Setting |
| :---: |  :---: |  :---: |  :---: |  :---: | 
| 0 | 1500 | 0.7 | 1000 | N15_M07_F10 |
| 1 | 900 | 0.7 | 1000 | N09_M07_F10 | 
| 2 | 1500 | 0.1 | 1000 | N15_M01_F10 |
| 3 | 1500 | 0.7 | 400 | N15_M07_F04 |

### Table 7. Operating parameter of healthy (undamaged)  bearings during run-in period.

| Bearing Code | Run-in Period [h] | Radial Load [N] | Speed [min^-1] |
|  :---: |  :---: |  :---: |  :---: | 
| K001 | >50 |  1000-3000 | 1500-2000 |
| K002 | 19 | 3000 | 2900 |
| K003 | 1 | 3000 | 3000 | 
| K004 | 5 | 3000 | 3000 | 
| K005 | 10 | 3000 | 3000 |
| K006 | 16 | 3000 | 2900  |

## 4.使用情况
* Bin Hasan M. Current based condition monitoring of electromechanical systems. Model-free drive system current monitoring: faults detection and diagnosis through statistical features extraction and support vector machines classification.[D]. University of Bradford, 2013.
* Lessmeier C, Kimotho J K, Zimmer D, et al. Condition monitoring of bearing damage in electromechanical drive systems by 
using motor current signals of electric motors: a benchmark data set for data-driven classification: Proceedings of the
European conference of the prognostics and health management society, 2016[C].[论文链接](https://mb.uni-paderborn.de/fileadmin/kat/PDF/Veroeffentlichungen/20160703_PHME16_CM_bearing.pdf)

* Pandhare V, Singh J, Lee J. Convolutional Neural Network Based Rolling-Element Bearing Fault Diagnosis for Naturally Occurring and Progressing Defects Using Time-Frequency Domain Features[C]//2019 Prognostics and System Health Management Conference (PHM-Paris). IEEE, 2019: 320-326.[论文链接](https://ieeexplore.ieee.org/abstract/document/8756423)

* Zhu Z, Peng G, Chen Y, et al. A convolutional neural network based on a capsule network with strong generalization for bearing fault diagnosis[J]. Neurocomputing, 2019, 323: 62-75.[论文链接](https://www.sciencedirect.com/science/article/pii/S0925231218311238)  
基于强泛化胶囊网络的卷积神经网络用于轴承故障诊断

* Chen Y, Peng G, Xie C, et al. ACDIN: Bridging the gap between artificial and real bearing damages for bearing fault diagnosis[J]. Neurocomputing, 2018, 294: 61-71.[论文链接](https://www.sciencedirect.com/science/article/pii/S092523121830300X)
ACDIN:弥补人工与真实轴承损伤之间的差距，用于轴承故障诊断  

* Wu, J., et al., Sensors Information Fusion System with Fault Detection Based on Multi-Manifold Regularization Neighborhood Preserving Embedding. Sensors, 2019. 19(6): p. 1440. [论文链接](https://www.mdpi.com/1424-8220/19/6/1440)
基于多流形正则化保邻域嵌入的传感器信息融合系统  


## 


[<<返回主目录](../README.md)
