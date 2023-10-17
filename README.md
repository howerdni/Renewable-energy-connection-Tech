# -
对新能源，包括风电，光伏等最新（电力电子）并网系统进行阐述
# 风力机关键技术
## 简介
迄今为止，风能仍然是最具前景的可再生能源之一，因为它具有相对较低的能源成本。风力机系统（WTS, wind turbine system）技术始于上世纪80年代，当时功率仅为几十千瓦，而如今通常安装的是多兆瓦（MW）级别的风力涡轮机，其尺寸仍在不断增长。风力（叶轮）机（wind turbine）已经在配电网络中得到了广泛应用，现在越来越多的风力发电站正在接入输电网，充当传统发电厂的角色。例如，丹麦的风力发电渗透率很高，如今丹麦的电能超过30%都由风能提供。

最初，风机接入并未对电力网系统产生严重影响，风机解决方案采用基于鼠笼式感应发电机（SCIG，squirrel-cage inducton generator）的技术，直接连接到电网，因此风中的功率脉动几乎直接传递到电网中。此外，对于所提供的有功和无功功率（调节电网系统的频率和电压方面重要的控制参数）没有可控性。如今，随着风机渗透率和功率水平的急剧增加，风能对电网运行产生了显著影响。目前基于电力电子技术的风机并网解决方案已经成为主流；这主要是因为电力电子技术可以将风机的特性从一个不受调控的电源转变为一个主动可控的电源。值得一提的是，用于风机的电力电子技术并不是新技术，但必须仔细考虑到在其在风机并网应用中的一些特殊要求。
## 风能变换器
风力发电系统通过空气动力学叶片捕获风能，并将其转换为发电机轴上的旋转机械功率。为了实现合理的功率转换，叶片的端速度应低于声速的一半，因此随着叶片直径的增加，旋转速度会降低。对于典型的兆瓦级风机，旋转速度在5~16r/min之间变化，这可能导致发电机过于笨重并可能增加安装成本。目前将低速高扭矩的机械功率转换为有效功率的减重解决方案之一是使用齿轮箱，如图所示。

如今，具有大型齿轮箱和部分功率电力变换器的高速双馈感应发电机（DFIG, doubly fed induction generator）主导了市场，但在未来，为了取得最佳整体性能，采用多极永磁同步发电机（PMSGs, permanent magnet synchronous generators）和具有更简单或不需要齿轮箱，并使用全功率电力变换器的方案将会成为主流。实际上，具有外部励磁或永磁体的同步发电机正在成为风力机更受青睐的技术。
