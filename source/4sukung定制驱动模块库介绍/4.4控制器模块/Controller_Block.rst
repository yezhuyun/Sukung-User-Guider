
4.4.1 一阶、二阶LADRC模块
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

    以二阶LADRC为例，介绍此模块使用方式：

    ``2-Order LADRC`` 模块是针对典型二阶对象所设计的线性自抗扰控制器（ ``1-order LADRC`` 模块类似，在此不再赘述），请参考 :ref:`线性自抗扰控制` 。

    详细内容请自行查看相关ADRC资料，推荐\ `B站 <https://space.bilibili.com/408884199/>`__\ 和自抗扰控制QQ群(128464029(入门)，模块通过参考输入 ``r`` 和 被控对象输出 ``yp`` 产生控制量 ``u`` 以及扩张观测器的观测状态 ``xo1`` 、 ``xo2`` 和  ``xo3``。使用模块(控制方法)需要对模块参数进行配置:

        - ``ESO Bandwidth wo``：扩张状态观测器的带宽参数 :math:`{{\omega _0}}` ，其决定了ESO的跟踪速度，此值越大，ESO估计扰动越快，但过大可能导致噪声难以忍受或ESO振荡；
        - ``Conreoller Bandwidth wc``：控制器带宽 :math:`{{\omega _c}}` ，其决定了控制器的响应速度，一定范围内越大控制效果越好，但过大可能使系统不稳定，需要根据瞬态响应进行调节；
        - ``Control Variable b0``：控制量增益 :math:`{b_0}` ,其代表了对象的特性，可以由阶跃响应中的初始加速度导出。

    .. figure:: Controller_Media/1O_LADRC.PNG
        :align: center
        :scale: 100%




4.4.2 二阶Adaptive ADRC模块
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

    ``2-Order Adaptive ADRC`` 模块是在二阶线性自抗扰控制器基础上增加“定量自适应”调节机制，有兴趣可以查看 `文献 <https://xueshu.baidu.com/usercenter/paper/show?paperid=1k7r0gp0cy5002r07k3r0vg03w394442&site=xueshu_se>`_  。在此对其使用进行说明

    方法根据参考模型 :math:`\frac{{\omega _c^2}}{{{{\left( {s + {\omega _c}} \right)}^2}}}` 与ESO的观测状态( :math:`{x_{o1}}` 、:math:`{x_{o2}}`)之间的跟踪误差 :math:`{e_r} = {P_1}{e_{r1}} + {P_2}{e_{r2}}`，经鲁棒自适应律对 ``2-Order LADRC`` 模块的控制器参数进行自适应调节保证被控对象状态能够跟踪参考模型。

        - ``Controller Bandwith wc``：控制器带宽 :math:`{{\omega _c}}` ，调参方式与LADRC一致；
        - ``ESO Bandwidth wo``：扩张状态观测器的带宽参数 :math:`{{\omega _0}}` ，调参方式与LADRC一致；
        - ``Control Variable b0``：控制量增益 :math:`{b_0}` ,调参方式与LADRC一致；
        - ``Adaptive Scheme Bandwidth wa``：自适应带宽 :math:`{\omega _A}` ，其决定自适应的速率，一般大于 :math:`{\omega _o}` ;
        - ``Quantitative Gain q``：定量自适应调节参数 :math:`q` ，当设置 :math:`q=0` ，其退化为LADRC，在LADRC的基础上逐步定量增大 :math:`q` ，以引入自适应机制，提高动态性能；
        - ``Tracking Error Gain P1``：跟踪误差加权系数 :math:`{P_1}` ，跟踪误差 :math:`{e_r}` 中 :math:`{e_{r1}}` 的比重；一般推荐设置为10；
        - ``Tracking Error Differential Gain P2``：跟踪误差微分加权系数 :math:`{P_2}` ，跟踪误差 :math:`{e_r}` 中 :math:`{e_{r2}}` 的比重；一般推荐设置为1。
    
    .. figure:: Controller_Media/2O_AdaptiveADRC.PNG
        :align: center
        :scale: 100%



4.4.3 DR-PID 模块
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  
    根据 :ref:`DRPID` ，封装了 ``DR-PID`` 模块，对应的参数配置可参考此章节，在此不再赘述。

    .. figure:: Controller_Media/DRPID.PNG
        :align: center
        :scale: 100%