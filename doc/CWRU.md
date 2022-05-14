# CWRU数据说明
## 1.概述

​      CWRU数据集美国凯斯西储大学提供。截止到 2015 年，仅机械故障诊断领域顶级期刊《Mechanical Systems and Signal Processing》就发表过 41 篇使用CWRU 轴承数据进行故障诊断的文章。在基于深度学习的轴承故障诊断领域。当下，轴承故障诊断算法更新较快，为了评价被提出算法的优越性，最客观的方式就是使用第三方标准数据库与当下主流算法比较。试验中使用2马力Reliance Electric电动机进行实验，并且在靠近和远离电动机轴承的位置处测量加速度数据。每个实验都仔细记录了电机的实际测试条件以及轴承故障状态。
使用电火花加工（EDM）为电机轴承提供故障。在内滚道，滚动元件（即滚珠）和外滚道处分别引入直径0.007英寸至0.040英寸直径的故障。将故障轴承重新安装到测试电机中，并记录0至3马力（电机速度为1797至1720 RPM）的电机负载的振动数据。


* 数据下载连接(https://csegroups.case.edu/bearingdatacenter/pages/welcome-case-western-reserve-university-bearing-data-center-website)
CWRU数据集是使用最为广泛的，文献较多。不一一举例。其中University of New South Wales 的Wade A. Smith在2015年进行了比较全面的总结和对比。比较客观的综述和分析了使用数据进行诊断和分析研究的情况。官方网站提供的是.mat格式的数据，MATLAB直接使用比较方便。
* Github上有人分享了在python中自动下载和使用的方法。https://github.com/Litchiware/cwru
* R语言中使用的方法：https://github.com/coldfir3/bearing_fault_analysis


## 2.试验条件
​        CWRU轴承数据集采集实验台由1.5kW的电机、驱动端轴承、风扇端轴承、扭矩传感器、测功机、加速度传感器和电子控制器组成。待检测的轴承支撑着电动机的转轴，驱动端轴承型号为SKF6205，风扇端轴承型号为SKF6203，本文中使用驱动端轴承数据集。通过电火花加工模拟轴承的多种健康状况，电动机风扇端和驱动端的轴承座上方各放置一个加速度传感器用来采集故障轴承的振动加速度信号。振动信号通过16通道的数据记录仪采集得到，采样频率为12kHz，功率和转速通过扭矩传感器测得。

## 3.数据基本情况
​			该数据集包括四种轴承不同轴承健康状态，即**正常状态、内圈故障、外圈故障和滚动体故障**。分别有7mils、14mils和21mils**三种故障直径**（1mils=0.0254mm）。该电动机在0hp、1hp、2hp、3hp**四种不同的负载**和1730r/min、1750r/min、1772r/min、1797r/min**四种不同转速**下收集振动信号。
### 基准研究
* Smith W A, Randall R B. Rolling element bearing diagnostics using the Case Western Reserve University data: A benchmark study[J]. Mechanical Systems and Signal Processing, 2015,64-65:100-131.[论文链接](https://www.sciencedirect.com/science/article/pii/S0888327015002034)
* Boudiaf A, Moussaoui A, Dahane A, et al. A comparative study of various methods of bearing faults diagnosis using the case Western Reserve University data[J]. Journal of Failure Analysis and Prevention, 2016, 16(2): 271-284. [论文链接](https://link.springer.com/article/10.1007/s11668-016-0080-7)
### 信号处理与特征工程

 * Su W, Wang F, Zhu H, et al. Rolling element bearing faults diagnosis based on optimal Morlet wavelet filter and autocorrelation enhancement[J]. Mechanical systems and signal processing, 2010, 24(5): 1458-1472.[论文链接](https://www.sciencedirect.com/science/article/pii/S0888327009003835)  
 基于最优小波滤波和自相关增强的滚动轴承故障诊断方法

 * Saidi L, Ali J B, Fnaiech F. Bi-spectrum based-EMD applied to the non-stationary vibration signals for bearing faults diagnosis[J]. ISA transactions, 2014, 53(5): 1650-1660.[论文链接](https://www.sciencedirect.com/science/article/pii/S0019057814001220)  
 基于双谱的emd应用于非平稳振动信号的轴承故障诊断  

 * Zhu K, Song X, Xue D. A roller bearing fault diagnosis method based on hierarchical entropy and support vector machine with particle swarm optimization algorithm[J]. Measurement, 2014, 47: 669-675.[论文链接](https://www.sciencedirect.com/science/article/pii/S0263224113004569)  
 提出了一种基于层次熵和支持向量机的滚动轴承故障诊断方法

 * Li Y, Wang X, Si S, et al. Entropy based fault classification using the Case Western Reserve University data: A benchmark study[J]. IEEE Transactions on Reliability, 2019.[论文链接](https://ieeexplore.ieee.org/abstract/document/8662701)  
 基于熵的故障分类利用西储大学案例数据:一项基准研究  

 * Kedadouche M, Liu Z, Vu V H. A new approach based on OMA-empirical wavelet transforms for bearing fault diagnosis[J]. Measurement, 2016, 90: 292-308.[论文链接](https://www.sciencedirect.com/science/article/pii/S0263224116301361)  
 提出了一种基于经验小波变换的轴承故障诊断方法 


### 分类与识别

* Raj A S, Murali N. Early classification of bearing faults using morphological operators and fuzzy inference[J]. IEEE Transactions on Industrial Electronics, 2012, 60(2): 567-574.[论文链接](https://ieeexplore.ieee.org/abstract/document/6153367)  
利用形态算子和模糊推理对轴承故障进行早期分类

* Afrasiabi S, Afrasiabi M, Parang B, et al. Real-Time Bearing Fault Diagnosis of Induction Motors with Accelerated Deep Learning Approach[C]//2019 10th International Power Electronics, Drive Systems and Technologies Conference (PEDSTC). IEEE, 2019: 155-159.[论文链接](https://ieeexplore.ieee.org/abstract/document/8697244)  
采用加速深度学习方法对异步电机轴承故障进行实时诊断 

* Zhang R, Tao H, Wu L, et al. Transfer learning with neural networks for bearing fault diagnosis in changing working conditions[J]. IEEE Access, 2017, 5: 14347-14357.[论文链接](https://ieeexplore.ieee.org/abstract/document/7961149)  
基于神经网络的轴承故障转移学习方法，用于轴承在不同工况下的故障诊断

## 3.数据特点
 人为制造的故障，特征明显，诊断相对容易。使用广泛，认可度高。可以作为算法检验的基础数据集。


[<<返回主目录](../README.md)
