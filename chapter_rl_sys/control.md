## 控制系统

虽然控制理论已牢牢植根于基于模型（Model-based）的设计传统，但丰富的数据和机器学习给控制理论带来了新的机遇。控制理论和机器学习的交叉点涵盖了广泛的研究方向，包括但不限于动态系统的学习、在线学习和控制、深度学习的控制理论观点、强化学习以及在各种现实世界系统中的应用。
从机器学习的角度来看，未来的主要挑战之一是超越模式识别并解决数据驱动控制和动态过程优化方面的问题。

理论方面，线性二次控制（Linear-Quadratic
Control）是经典的控制方法，最近有关于图神经网络在分布式线性二次控制的研究 :cite:`pmlr-v144-gama21a`。作者称将线性二次问题转换为自监督学习问题，能够找到基于图神经网络（Graph
Neural
Networks，GNN）的最佳分布式控制器，他们还推导出了所得闭环系统稳定的充分条件。随着基于数据和学习的机器人控制方法不断得到重视，研究人员必须了解何时以及如何在现实世界中最好地利用这些方法，因为安全是至关重要的，有的研究通过学习不确定的动力学来安全地提高性能，鼓励安全或稳健的强化学习方法，以及可以正式认证所学控制策略的安全性的方法 :cite:`brunke2021safe`。图:numref:`safe\_learning\_control`展示了安全学习控制（Safe Learning
Control）系统的框架图，用数据驱动的方法来学习控制策略，兼顾安全性。Lyapunov :cite:`pmlr-v144-mehrjou21a`
函数是评估非线性动力系统稳定性的有效工具，最近有人提出Neural
Lyapunov来将安全性纳入考虑。

应用方面，有基于神经网络的自动驾驶汽车模型预测控制 :cite:`vianna2021neural`，也有研究将最优控制和学习相结合并应用在陌生环境中的视觉导航 :cite:`pmlr-v100-bansal20a`，该研究将基于模型的控制与基于学习的感知相结合来解决。基于学习的感知模块产生一系列航路点通过无碰撞路径引导机器人到达目标。基于模型的规划器使用这些航路点来生成平滑且动态可行的轨迹，该轨迹使用反馈控制在物理系统上执行。在模拟的现实世界杂乱环境和实际地面车辆上的实验表明，与纯粹基于几何映射或基于端到端学习的替代方案相比，这种新的系统可以在新环境中更可靠、更有效地到达目标位置。强化学习和模仿学习与控制论有密切联系：LEOC :cite:`pmlr-v144-zhang21b`整合了强化学习和经典控制理论的原则方法。有人将基于模型的离线强化学习算法扩展到高维视觉观察空间并在真实机器人上执行基于图像的抽屉关闭任务方面表现出色 :cite:`pmlr-v144-rafailov21a`。控制部分通过神经网络优化可以更加平滑、节能、安全，如何将
神经网络和传统控制理论结合，特别是和运动学算法相结合，将会是一个有趣的方向。

![安全学习控制系统，数据被用来更新控制策略或或安全滤波器 :cite:`brunke2021safe`](../img/ch13/safe_learning_control.png)

:width:`800px`

:label:`safe\_learning\_control`
