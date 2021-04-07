.. Sukung User Guider documentation master file, created by
   sphinx-quickstart on Fri Mar 26 14:40:49 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

===================================
嵌入式实时半实物仿真平台Sukung
===================================


前言
====

   Sukung是由华侨大学先进控制实验室研发的一类嵌入式实时半实物仿真平台。它由聂卓赟副教授指导，李兆洋(研究生)主导研发，程前(研究生)完善维护，可用于自动化、控制科学与工程及相关专业学科的理论实践教学、专业实验教学、课程设计、毕设科创等教学实践环节，也可用于科学研究、机器人原型系统设计、工业系统算法测试等应用场景。

   Sukung课题组选用MATLAB/Simulink作为仿真平台、STM32作为嵌入式目标机，研制了simulink和目标机之间各类资源调用的实时接口。Sukung拥有丰富的外设资源，包括：常用通信接口(USART，I2C，SPI，CAN)，常用IO/计数模块(DAC，ADC，ADC_Ex，GPIO，TIM，PWM，计数器)和专用外设接口(MPU6050，电子罗盘GY271，超声波传感器，显示屏TFT-LCD)等，能够帮助用户快速地开展“实时数据采集与传输”、“快速控制原型”、“硬件在环”和“在线监督优化”等实验。

   .. image:: media/image1.png
      :align: center
      :scale: 35 %

------------

   Sukung构建的一种典型半实物仿真平台如上图所示。图中，宿主机作为仿真平台用于控制算法仿真和目标机控制，仿真模型可在MATLAB/Simulink环境下通过代码生成部署的方式下载至目标机中运行。目标机为仿真模型提供实时运行环境和对象实时接口。

   结合嵌入式实时半实物仿真平台Sukung，常用的各类传感器和执行器可以在MATLAB/Simulink环境下进行调用。下图给出了基于Sukung的部分实验系统。

   .. image:: media/image2.jpg
      :align: center
      :scale: 35 %

软件获取与咨询
================

   当前软件版本：Sukung V1.0，有线下载，有线数据传输。:ref:`快速开始` Sukung。

   -  软件下载：`github <https://github.com/yezhuyun/Sukung-Setup>`_ 

   -  淘宝网址： `淘宝网址 <https://item.taobao.com/item.htm?id=641308134185>`_ 

   -  定制与合作请联系： yezhuyun@sukung.cn;

   -  技术问题可入群交流：
   -  
      Sukung半实物仿真技术交流，QQ群：661419695；

         .. image:: media/image268.png
            :align: center
            :scale: 55 %

.. toctree::
   :maxdepth: 1
   :caption: 目录:
   
   1什么是sukung/index
   2平台配置/index
   3平台使用/index
   4sukung定制驱动模块库介绍/index
   5案例/index
   6其他/index


