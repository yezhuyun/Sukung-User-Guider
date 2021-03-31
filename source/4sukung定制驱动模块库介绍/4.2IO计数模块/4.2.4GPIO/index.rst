.. Sukung User Guider documentation master file, created by
   sphinx-quickstart on Fri Mar 26 14:40:49 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. _GPIO:

4.2.4 GPIO 
~~~~~~~~~~

   此模块包括两个子模块：GPIO_Write模块和GPIO_Read模块，过此模块实现对引脚电平和数据的读和写。GPIO 最简单的功能是输出高低电平，同时GPIO还可以被设置为输入功能，用于读取按键等输入信号。为了实现不同工作条件要求，GPIO 共有8 种工作模式

      • 输入浮空——既不上拉也不下拉，可以做KEY 识别
      • 输入上拉——IO 内部上拉电阻输入
      • 输入下拉——IO 内部下拉电阻输入
      • 模拟输入——应用ADC 模拟输入，或者低功耗下省电
      • 开漏输出——需要外接上拉电阻才能输出高电平
      • 推挽输出——输入值是未知的
      • 推挽复用——片内外设功能（I2C 的SCL，SDA）
      • 开漏复用——片内外设功能（TX1，MOSI，MISO.SCK.SS）


.. toctree::
   :maxdepth: 2
   :caption: 目录：
   
   GPIO_Read
   GPIO_Write
   



