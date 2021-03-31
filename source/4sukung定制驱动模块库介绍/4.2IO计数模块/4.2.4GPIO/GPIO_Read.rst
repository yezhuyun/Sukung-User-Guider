(1) GPIO_Read模块
------------------------

   通过 ``GPIO_Read`` 模块，用户可以实现对电平的高低读取，并进行输出。为了实现功能，用户需要了解以下参数的含义以及设置

      • ``GPIO Port``：选择GPIO 模块的字母引脚
      • ``Pin Index``：选择对应字母下的数字编号
      • ``GPIO Mode``：选择GPIO 的工作模式
      • ``GPIO Pull``：选择对GPIO 引脚的上拉下拉
      • ``Sample Time`` ：采样时间，推荐与系统步长一致

   .. image:: media/image73.png
      :align: center
      :scale: 70 %  

**GPIO_Read模式下输入输出功能选择**

   .. image:: media/image74.png
      :align: center
      :scale: 70 %

GPIO_Read 功能选择界面，从上到下分别对应默认输入，输入上拉，输入下拉，输入浮空。其中IT 能够出发中断，EVT 只能设置中断标志位，不产生中断。当选择了IT_RISING（FALLING）时，需要在GPIO_Pull中选择对应的PLULLUP（PULLDOWN），使用INPUT 或者RISING_FALING时使用NOPULL

.. image:: media/image75.png
   :align: center
   :scale: 70 %