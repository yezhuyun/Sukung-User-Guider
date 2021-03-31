.. Sukung User Guider documentation master file, created by
   sphinx-quickstart on Fri Mar 26 14:40:49 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. _模块介绍:

4. Sukung定制驱动模块库介绍
===========================

   在安装完成Sukung后，用户会在Simulink Library Browse中看到Sukung定制驱动模块库，如下图所式。这些定制驱动模块包括 ``AD`` (模数转换模块)、 ``DA`` (数模转换模块)、 ``Counter`` (编码器模块)、 ``Display`` (液晶屏模块)、 ``I2C`` (I2C通讯模块)、 ``IO`` (输入输出模块)、 ``PWM`` (PWM模块)、 ``Sensor`` (传感器模块)等。

   通过定制驱动模块库，用户可以使用目标机的外设资源，快速搭建基于Sukung目标环境的系统模型，有效降低半实物仿真平台Sukung的使用门槛。接下来将分别对Sukung各模块进行介绍，让用户了解如何使用Sukung模块。我们也基于上述模块，制作了各种控制案例，详情参见 :ref:`演示案例`

   .. image:: Block_Media/image1.png
      :align: center
      :scale: 100 %

.. toctree::
   :maxdepth: 2
   :caption: 目录:
   
   4.1通讯模块/index
   4.2IO计数模块/index
   4.3定制板载模块/index
   4.4控制器模块/index

