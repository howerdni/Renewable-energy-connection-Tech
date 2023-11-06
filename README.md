# 新能源并网技术
对新能源，包括风电，光伏等最新（电力电子）并网系统进行阐述
# 1、风力机关键技术
## 1.1、简介
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;迄今为止，风能仍然是最具前景的可再生能源之一，因为它具有相对较低的能源成本。风力机系统（WTS, wind turbine system）技术始于上世纪80年代，当时功率仅为几十千瓦，而如今通常安装的是多兆瓦（MW）级别的风力涡轮机，其尺寸仍在不断增长。风力（叶轮）机（wind turbine）已经在配电网络中得到了广泛应用，现在越来越多的风力发电站正在接入输电网，充当传统发电厂的角色。例如，丹麦的风力发电渗透率很高，如今丹麦的电能超过30%都由风能提供。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;最初，风机接入并未对电力网系统产生严重影响，风机解决方案采用基于鼠笼式感应发电机（SCIG，squirrel-cage inducton generator）的技术，直接连接到电网，因此风中的功率脉动几乎直接传递到电网中。此外，对于所提供的有功和无功功率（调节电网系统的频率和电压方面重要的控制参数）没有可控性。如今，随着风机渗透率和功率水平的急剧增加，风能对电网运行产生了显著影响。目前基于电力电子技术的风机并网解决方案已经成为主流；这主要是因为电力电子技术可以将风机的特性从一个不受调控的电源转变为一个主动可控的电源。值得一提的是，用于风机的电力电子技术并不是新技术，但必须仔细考虑到在其在风机并网应用中的一些特殊要求。
## 1.2、风能变换器
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;风力发电系统通过空气动力学叶片捕获风能，并将其转换为发电机轴上的旋转机械功率。为了实现合理的功率转换，叶片的端速度应低于声速的一半，因此随着叶片直径的增加，旋转速度会降低。对于典型的兆瓦级风机，旋转速度在5~16r/min之间变化，这可能导致发电机过于笨重并可能增加安装成本。目前将低速高扭矩的机械功率转换为有效功率的减重解决方案之一是使用齿轮箱，如图所示。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;如今，具有大型齿轮箱和部分功率电力变换器的高速双馈感应发电机（DFIG, doubly fed induction generator）主导了市场，但在未来，为了取得最佳整体性能，采用多极永磁同步发电机（PMSGs, permanent magnet synchronous generators）和具有更简单或不需要齿轮箱，并使用全功率电力变换器的方案将会成为主流。实际上，具有外部励磁或永磁体的同步发电机正在成为风力机更受青睐的技术。目前影响技术的使用逻辑的更多的是价格的趋势变化。在电网和发电机之间插入电力变换器对风机系统的容量和损耗有关键性的作用。风力机和电网直接还需要使用到升压变，目前升压变部分也在更多的引入电力电子技术。
![1697512217638](https://github.com/howerdni/-/assets/28687425/52be3f9c-bb38-422b-9c6f-11fd6917e5c2)

## 1.3、风力机的基本控制变量
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;对于风力机系统，如何控制高风速下的机械功率，对于防止系统过载至关重要。功率控制可以通过失速控制（stall control）（桨叶固定在轮毂上，达到额定速度后，桨叶会被动发生失速），主动失速控制（activestall control）（桨叶在轮毂上可以活动，达到额定速度后，桨叶会主动调整角度发生失速）和桨距角控制（pitch control）。三种控制的特性如图。
![1697533126979](https://github.com/howerdni/-/assets/28687425/b2392ddb-9ea4-4113-8ad2-5c6053f910c1)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;另一个控制变量是风机叶片的转速，在过去，这个变量并不能自由控制，它在整个运行风速变化区间内都维持固定。虽然恒速风机系统具有一些优点，如简单，可靠，电气部分成本低等，但是缺点则更为显著，如无法控制有功无功，阵风天气下机械应力大，电能质量欠佳等。现在变速风机系统已经被广泛使用，因为它能提供更好的气动效率和控制性能。变速风机可以使得桨叶转速适应风速的变化，将叶尖速比维持恒定，从而最大效率的从风能中汲取电能，而风速的变化引起的风能变化可以在转子的速度变化过程中被吸收，这样机械应力和噪音都能得到降低。此外，电力变换器对转速的调节作用，也能使风机具有更好的可控性，这能满足电网对风机的更高的技术需求。这些特性正在成为未来的电网发展中决定性的因素。
## 1.4、风机概念
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在过去的30年里，用于风力发电系统（WTS）的解决方案也发生了巨大变化，出现了四到五代不同的技术，如图所示。通常，现有的风力机系统结构可以分为四个概念。这些概念之间的主要区别在于发电机的类型、电力电子、速度可控性以及限制气动功率的方式。
### 1.4.1、恒速风机（WT type A）
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;如图所示，这种布局结构对应于上世纪80年代非常流行的所谓的丹麦概念。风力机配备了一个异步鼠笼式感应发电机（SCIG），通过加入一个软启动器可以实现更平稳的电网连接，在正常发电模式下会旁路软启动器。
![image](https://github.com/howerdni/-/assets/28687425/d100b51f-6709-48e1-9655-03575263b25c)  
图 恒速风机的软启动并网  
这种早期的并网方案的缺点是需要配置无功补偿装置来补偿异步机的无功，由于转子的转速是不加任何控制的，这要求机械部分的强度足够大，以承受机械反向转矩，而风速的波动也会直接转化成电气的脉冲，这在比较弱的电网中可能导致电压的不稳定和效率的不稳定。
### 1.4.2、变速风机-变阻转子（WT type B）
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;如图 所示，这个概念也被称为OptiSlip（Vestas™），并在1990年代中期出现。它引入了可变转子阻力，从而限制风力发电机的速度，提高可控性。通常使用绕线式转子感应发电机（WRIG）和相应的电容补偿器，并通过软启动器将发电机直接连接到电网，与A型概念一样。这个概念的技术改进是，通过动态改变转子阻力可以部分调整风力发电机的转速。这个特性有助于减轻机械应力并使电力输出更加平稳。然而，在转子电阻中产生的恒定功耗是这个概念的一个重要缺点。
![image](https://github.com/howerdni/-/assets/28687425/b4c7820b-a390-4d5f-9b0f-4840adc5d9e2)  
图 变速风机带变阻转子的软启动并网  
### 1.4.3、变速风机-部分功率换流（WT type C）
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;目前，这个概念是最成熟的解决方案，自世纪初以来已被广泛应用。如图6.8所示，采用了一个与双馈感应发电机（DFIG）配套的反变频电力变换器。DFIG的定子绕组直接连接到电网，而转子绕组通过电力变换器连接到电网，通常其容量为风力发电机容量的30%。
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;通过使用电力变换器，可以灵活调节转子中的频率和电流，从而进一步扩展可变速范围，达到令人满意的水平。同时，电力变换器可以部分调节发电机的输出功率，改善电力质量并提供有限的电网支持。较小的变频器容量使得这个概念在成本方面具有吸引力。然而，其主要缺点是需要使用滑环，并在电网故障的情况下功率可控性具有一定的难度；这些劣势可能会抵消可靠性表现，并且可能无法满足未来的电网要求。
![image](https://github.com/howerdni/-/assets/28687425/4cf39172-c6ea-4f9e-81cb-8e4bee332a29)  
### 1.4.4、变速风机-全功率换流（WT type D）
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;另一个备受关注的概念，正在成为新开发和安装的风力发电机中越来越受欢迎，如图 所示。它引入了一个全功率变换器来连接电网和发电机的定子绕组；因此，所有由风力发电机产生的电力都可以进行调节。在这个概念中，目前被报导使用的技术已经涉及了AG、绕组转子同步发电机（WRSG）和永磁同步发电机（PMSG）。
相对于基于DFIG的概念，这个解决方案的主要优势包括消除了滑环，更简单的结构（取消了变速箱），全功率和速度可控性，以及更好的电网支持能力。由于使用了全功率变换器，功率转换阶段的电压级别可以灵活调节。未来，电压可能会足够高，可以直接连接到电网，而无需庞大的低频变压器，这一优势可能是未来风力发电系统吸引人的特性之一。然而，更加紧张和昂贵的电力电子以及永磁材料的价格可能会对这个概念在进一步商业化方面带来一些不确定性。
![image](https://github.com/howerdni/-/assets/28687425/a20128e1-0768-4ba2-9a7b-9f6fb1e5e8ff)  
<p align="center">
图 全功率换流器 
</p> 

### 1.4.5、不同风机系统的结构对比 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;对比不同的风机系统解决方案揭示了成本与性能之间的矛盾。表 显示了四种涡轮概念的电网侧控制、成本、维护和内部涡轮性能的比较[11]。可以看出，由于使用了电力电子变流器，C型和D型风力涡轮系统在转速、控制带宽和交/直流功率传递方面比A型和B型方案实现了更好的功率可控性。此外，明显可见C型和D型风力涡轮概念在连接电网时具有许多重要特性，因此它们更适合与电网集成。考虑到近几十年来电力半导体器件的价格一直在不断降低，为了，C、D型号的结构将会取代A,B成为主流。   
 
|System|Type A|Type B|Type C|Type D|
|---|---|---|---|---|
|Variable speed|No|No|Yes|Yes|
|Control active power|No|No|Yes|Yes|
|Control reactive power|Limited|Limited|Yes|Yes|
|Short circuit (fault-active)|No|No|No/yes|Yes|
|Short circuit power|Contribute|Contribute|Contribute|Limit|
|Control bandwidth|1–10 s|100 ms|1 ms|0.5–1 ms|
|Standby function|No|No|Yes+|Yes++|
|Flicker (sensitive)|Yes|Yes|Yes|No|
|Soft starter needed|No|No|Yes|Yes|
|Rolling capacity on grid|Yes, partly|Yes, partly|Yes|Yes|
|Reactive compensator (C)|Yes|Yes|No|No|
|Island operation|No|No|Yes/no|Yes|
|Investment|++|++|+|0|
|Maintenance|++|++|0|+|
## 1.5、风机的电力变换器
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;变换器联系机侧和网侧，在机侧，其电流应该得到控制，以调节转矩进而调节风机的转速。这个控制，在正常运行时，即最大风能跟踪控制时，以及在故障时，都有助于有功功率的平衡。同时换流器也需要有能力调节发电机机端的基频附近变化的频率和电压幅值。  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在网侧，换流器需要满足电网的要求，即功率上能控制无功的输出，有功能做到快速响应，频率和电压上能够维持一个恒定值，谐波能维持一个较小的值。
### 1.5.1、风机变换器的拓扑结构
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;大于两电平的变换器称为多电平变换器，常见的时3电平和5电平；从原理上可以分为中性点钳位和H桥两种大类。
![image](https://github.com/howerdni/Renewable-energy-connection-Tech/assets/28687425/87c7e3f5-aa8d-4a45-beb4-4c53aeaa5536)  
<p align="center">
 Three-level neutral-point clamped back-to-back converter for wind turbine (3L-NPC BTB)
</p>

![image](https://github.com/howerdni/Renewable-energy-connection-Tech/assets/28687425/3e9b915f-88e9-4fe6-bbeb-430faed454a6)  
<p align="center">
 Three-level H-bridge back-to-back converter for wind turbine (3L-HB BTB)
</p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;另外还有模块化多电平的换流器（MMC），他具有可扩展性好，谐波很小，可以取消滤波器等优势，但是最大的功率可能受限，电容直流电压的波动可能因为发电机侧的交流频率比较低而波动大，这会要求电容的容量需求更大。   

## 1.6、现代风机的控制和电网要求
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;目前讨论的风机控制主要是TypeC和TypeD类并网方案的风机，风机发出的有功，应该通过风机的机械部分去控制，同时整个控制系统应该满足调度的要求。更高级的控制还包括最大功率输出，故障穿越和点电网支撑的提供。
![image](https://github.com/howerdni/Renewable-energy-connection-Tech/assets/28687425/e809bd0a-078a-4529-8086-5c80165c9062)  
<p align="center">
 General control structure for modern wind turbines
</p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;变速风机的发电机电流，可以通过变流器控制，从而使得发电机转速调整到获得最大功率汲取的状态。而关于电网故障和支撑这方面，需要通过风机系统的各个子系统，例如网侧换流器，斩波电路，桨距角等。具体到更底层的控制的实现，例如电流控制，直流电压控稳定制，电网同步都能在换流器中实现，其中典型的控制环节是PI和PR控制（比例积分和比例谐振）。
随着风机的渗透率提供，风机的技术更新迭代，目前很多国家的风机接入电网的规范规程都在更新。随着风机接入电网的电压等级越来越高，电网越来越将风机接入的要求和传统发电机看齐，一般来说，电网主要从可控性，电能质量，故障穿越和电网支撑这几个角度来对风机系统提出要求。

## 1.7、双馈风力机的模型和控制
### 1.7.1、机电结构
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;双馈风力机系统的基本结构就是上述章节中的变速风机-部分功率换流（WT type C）描述的结构。
![image](https://github.com/howerdni/Renewable-energy-connection-Tech/assets/28687425/a1255ee3-ca54-46b0-8c6d-c66cb309788a)
<p align="center">
 General supply configuration of DFIM
</p>

### 1.7.2、稳态方程
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;定子的电气量角速度，转子的电气量角速度和转子的电气速度之间的关系如下：
```math
\omega_{s}=\omega_{r}+\omega_{m}\tag{1.1}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;转子的电气速度和机械速度的关系如下：
```math
\omega_{m}=p\Omega_{m}\tag {1.2}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;以上单位都是rad/s。转差率如下表示：
```math
\frac{\omega_{s}-\omega_{m}}{\omega_{s}} = \frac{\omega_{r}}{\omega_{s}}\tag {1.3}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;定子电气上直接和电网连接，所以$`\omega_{s}`$是恒定值（理论上），也就是同步速，显然，$`\omega_{r}`$取决于转子的转速，这样，按照转子的电气速度和同步速之间的关系，可以分为三种运行模式：
```math
\omega_{m}<\omega_{s}\Longrightarrow \omega_{r}>0 \Longrightarrow s>0 \Longrightarrow 次同步模式
```
```math
\omega_{m}>\omega_{s}\Longrightarrow \omega_{r}<0 \Longrightarrow s<0 \Longrightarrow 超同步模式
```
```math
\omega_{m}=\omega_{s}\Longrightarrow \omega_{r}=0 \Longrightarrow s=0 \Longrightarrow 同步模式
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;下面推导稳态方程：
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;定义电气量：
|Electric magnitudes of the stator and rotor|Electric parameters of the stator and rotor:|
|---|---|
|$`\underline{V_{s} }`$: Supplied stator voltage|$`R_{s}`$:Stator resistance($`\Omega `$)|
|$` \underline{V}_{r}^{'} `$: Supplied stator voltage|$` R_{r}^{'} `$:Rotor resistance($`\Omega `$)|
|$` \underline{I}_{s}^{} `$: Stator current|$` L_{m}^{} `$:Mutual inductance(H)|
|$` \underline{I}_{r}^{'} `$: Rotor current|$` L_{\sigma s}^{} `$:Stator leakage inductance(H)|
|$` \underline{E}_{s}^{ } `$: Induced emf in the stator|$` L_{\sigma r}^{'} `$:Rotor leakage inductance(H)|
|$` \underline{E}_{rs}^{' } `$: Induced emf in the rotor|$` N_{s}^{ },N_{r}^{ } `$:Stator,rotor windings, number of turns per phase|  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;定义绕组的匝数比：
```math
u=\frac{N_{s}}{N_{r}}\tag {1.4}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;于是定转子的磁链有如下关系：
```math
\underline{E}_{rs}^{' }=s\frac{\underline{E}_{s}}{u}\tag {1.5}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;下图给出双馈电机的单相电气模型：
![image](https://github.com/howerdni/Renewable-energy-connection-Tech/assets/28687425/bd892327-c04b-4d2d-b1ca-24ae3a50b1be)
<p align="center">
 One-phase steady-state equivalent electric circuit of the DFIM
</p>  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;为了分析方便，一般将参数按照下面转换后表示：
```math
R_{r}=R_{r}^{'}u_{}^{2}  \quad  L_{\sigma r}=L_{\sigma r}^{'}u_{}^{2}  \quad  \underline{I}_{r}^{}=\frac{\underline{I}_{r}^{'}}{u} \quad \underline{I}_{r}=\underline{I}_{r}{'}u \quad  E_{rs}=E_{rs}^{'}u
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;也就是带撇的参数是转子侧的实际参数，不带撇的参数是折算到定子侧的参数。于是，可以绘出等效单相稳态模型：
![image](https://github.com/howerdni/Renewable-energy-connection-Tech/assets/28687425/e12829bc-dd8f-410b-a048-8e87033a5d9f)  
<p align="center">
 One-phase steady-state equivalent electric circuit of the DFIM with rotor parameters, current and voltages
reduced to the stator
</p> 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;且进一步变换，可以使得定子侧和转子侧的频率一致，于是有：
