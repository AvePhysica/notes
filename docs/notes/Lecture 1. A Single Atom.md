## 1.1 电子能级结构

### 能级分层结构

我们考虑一个有 $Z$ 个电子的中性原子，其哈密顿量呈现出明显的能级分层结构，具体来说是：
- 电子与核之间的库伦相互作用。每个电子都在核子产生的库伦场中运动。其哈密顿量为：
$$
\hat H_0=\sum_{i=1}^Z\left(-\dfrac{\hbar^2\nabla_i^2}{2m^*}+V_{ei}(\vec r_i)\right)
$$
其中 $i=1,2,\cdots,Z$ 标记电子，$m^*$ 是约化质量，而 $V_{ei}(\vec r_i)=-Z\kappa/r$ 是核子与电子间的库伦势，其中 $\kappa=e^2/4\pi\varepsilon_0$。能量本征态为：
$$
E=-\dfrac{m^*Z^2\kappa^2}{2\hbar^2n^2}
$$
其仅取决于主量子数 $n$。这一能量大致在 $10^{14}\,\mathrm{Hz}$ 量级。
- 电子间的库仑相互作用。电子间存在排斥作用，哈密顿量为：
$$
\hat V_c=\sum_{i<j}V_{ee}(\vec r_i-\vec r_j)
$$
此时内层电子会屏蔽核产生的库伦场，使价电子感受到的库伦场降低，而向内逐渐恢复至 $-Z\kappa/r$ 。因此中心势不再具有 $r^{-1}$ 的正比关系，原子的 $SO(4)$ 对称性被破坏。能级现在还依赖于角量子数 $l$：
$$
E=-\dfrac{m^*Z^2\kappa^2}{2\hbar^2(n-\delta(n,l))^2}
$$
$\delta(n,l)$ 称为“**量子缺陷**”，其引起的能级劈裂同样在**电子伏特**量级。进一步的，对于双电子，由于对称的自旋波函数会导致反自旋的空间波函数，从而使空间上两电子相互远离而能量更低，因此三重态的能量低于单态。推广至多电子，会自然的推出当电子总自旋 $S$ 最大时能量最低，这实际上就是Hund第一规则。另外，对于给定的 $S$ 值，轨道角动量 $L$ 最大时会使电子进一步远离而能量更低，这是Hund第二规则。Hund定律的特征能量尺度同样为电子伏特。
- 精细结构。精细结构中的自旋-轨道耦合项的哈密顿量写为：
$$
\hat H_{so}=\sum_i\alpha_f^i\hat S_i\cdot \hat L_i
$$
其描述电子的轨道角动量与自旋角动量存在耦合。其可半经典地视为核子在电子本征系中产生的磁场与电子自旋磁矩相互作用的结果。其特征能量尺度为 $10^{-3}\,\mathrm{eV}(\sim 10^{11}\,\mathrm{Hz})$。在多数情形下，其比Hund规则的特征能量低得多。因此我们应当先由于电子库伦作用耦合得到总自旋角动量 $S$ 与轨道角动量 $L$ ，再由于精细结构耦合 $\vec L+\vec S=\vec J$，这称为 $L-S$ 耦合。但是，对于较重的原子，精细结构的强度很大甚至可以与Hund定律相比。此时应当先耦合每个电子总角动量 $\vec J_i=\vec L_i+\vec S_i$，再耦合总角动量 $\vec J=\sum_i \vec J_i$ 。这称为 $J-J$ 耦合。
- 超精细结构。超精细结构将电子角动量 $L,S$ 与核自旋 $I$ 耦合，其特征能量尺度为 $10^{-6}\,\mathrm{eV}(\sim 10^{8}\,\mathrm{Hz})$。因此我们可以先耦合得到 $\vec J$，再将其与 $\vec I$ 耦合。哈密顿量写为：
$$
\hat H_{hf}=\alpha_{hf}\hat J\cdot\hat I
$$
### 冷原子

至今，有三类原子已被冷却至量子简并状态，其分别是：
1. 碱金属元素(alkali-metal)。如氢(H)、锂(Li)、钠(Na)、钾(K)、铷(Rb)、和铯(Cs)
2. 碱土金属元素(alkali-earth-metal)。包括锶(Sr)、钙(Ca)和镱(Yb)。虽然镱不属于碱土金属，但其最外层价电子与碱土金属相似。
3. 具有大电子磁矩的原子，这里称为“磁性原子”，包括铬(Cr)、镝(Dy)和铒(Er)。
如下表所示。
 <div align="center">
  <img src="Pasted image 20251216231457.png" width="600">
</div>

- 碱金属元素。其基态只有一个在s层的价电子，term symbol为$^2S_{1/2}$。基态没有自旋-轨道耦合，但可以有超精细结构，如 $^{87}\mathrm{Rb}$ 有核自旋 $I=\frac32$，故总角动量为 $F=1,2$。而激发态为 $L=1$ ，term symbol 为 $^2P_{1/2},^2P_{3/2}$，两者能量劈裂由精细结构引起，且前者的能量更低（Hund第三规则）。超精细结构会让两者进一步劈裂。
- 碱土金属元素。基态为两个s层的价电子，其处于单态，因此 $L=S=0$。所有碱土金属原子的**玻色同位素**均具有零核自旋，而**费米同位素**则具有非零核自旋 $I$，其数值可能非常大。但由于 $J=0$，进而导致超精细耦合的缺失，核自旋与电子自旋自由度解耦。
  对于第一激发态，一个电子被激发至p层。由Hund规则，$S=1$ 的三重态能量将低于 $S=0$ 的单态，terms symbol分别为 $^3P_{0},^3P_{1},^3P_{2}$ 与 $^1P_{1}$。偶极跃迁不能改变 $S$，但是自旋轨道耦合可以耦合 $^3P_{1}$ 与 $^1P_{1}$。但是 $^3P_{0},^3P_{1},^3P_{2}$ 之间只能通过**超精细结构耦合**（对费米同位素而言），因此 $^3P_{0},^3P_{2}$ 有很长的寿命（可达数秒）。其可作为精细测量的工具，也可作为原子钟。对于玻色同位素而言，由于缺乏核自旋，$^3P_{0},^3P_{2}$态之间不存在单光子偶极跃迁。此时，它们与基态的耦合必须通过高阶过程实现。这两个量子态的寿命可达数年，在实际应用中可视为未发生衰变。

 <div align="center">
  <img src="Pasted image 20251216233523.png" width="600">
</div>

- 磁性原子。磁性原子有很大的总角动量 $J$，如铬的 $3d$ 与 $4s$ 轨道半充满，因此 $S=3$。在有限磁场的作用下，$J$ 易于极化，从而产生较大的磁矩。磁矩比碱金属原子的磁矩大约大一个数量级，从而两个原子之间的磁偶极相互作用也大两个数量级。

## 1.2 磁场能级结构

### Zeeman effect

现在，我们考虑静磁场引起的Zeeman效应。一般而言，实验室产生的磁场大致在几百个高斯左右，Zeeman效应的能级劈裂与超精细结构相当。以$^{87}\mathrm{Rb}$  原子的基态为例，其 $S=1/2,L=0,I=3/2$ ，Hamitonian写为：
$$
\hat H_s=B(\mu_Bg_S\hat S_z+\mu_Ng_I\hat I_z)+\alpha_{hf}\hat J\cdot\hat I
$$
其中 $\mu_B,\mu_N$ 为玻尔磁矩与核磁矩。由于核的质量远大于电子，因此 $\mu_N\ll \mu_B$。其Zeeman效应引起的能级劈裂如下图所示：

 <div align="center">
  <img src="Pasted image 20251217101622.png" width="600">
</div>

- 在左侧的低磁场区域，超精细项主导，能级分裂发生在 $F=1$ 与 $F=2$ 之间。
- 在右侧高磁场区域，电子自旋的Zeeman能主导，因此上面四条线为 $S_z=1/2$，下面四条线为 $S_z=-1/2$。而四条线内部的上下关系则由超精细项决定（注意此时核自旋的Zeeman能仍远小于超精细项），由于 $\alpha_{hf}>0$，因此上面四条线中 $I_z$ 大的能量高，因此 $F_z$ 从上到下依次递减，而下面四条线反之。

### Magnetic Trap

当有磁场存在时，一些自旋态的能量随磁场强度增大而升高，这类态称为"**low-field seeking**"原子 ，其会被束缚在磁场强度的局部极小值处。相反的，还有一些自旋态的能量随磁场强度增大而降低，这类态称为"**high-field seeking**"原子 ，其会被束缚在磁场强度的局部极大值处。这就是磁势阱的工作原理。然而，通过Maxwell方程可以验证，无电流分布的区域磁场不可能有局域极大值。

### 涌现出的规范场

考虑磁场中的原子，其薛定谔方程为：
$$
i\hbar\dfrac{\partial \psi}{\partial t}=\left(-\dfrac{\hbar^2}{2m}\nabla^2+\hat H_s(\vec r)\right)\psi
$$
即空间分布的磁场 $\vec B(\vec r)$ 会造成原子在不同位置感受到不同的哈密顿量 $\hat H_s(\vec r)$。
$$
\hat H_s=\mu_Bg_S\vec B(\vec r)\cdot\hat S+\mu_Ng_I\vec B(\vec r)\cdot\hat I+\alpha_{hf}\hat J\cdot\hat I
$$
现在我们希望将哈密顿量对角化，因此我们需要引入一个幺正算符场 $\mathcal U(\vec r)$。
$$
\tilde\psi(\vec r)=\mathcal U^\dagger(\vec r)\psi(\vec r),\quad \Lambda(\vec r)=\mathcal U^\dagger(\vec r)\hat H_s(\vec r)\mathcal U(\vec r)
$$
则新的运动方程为：
$$
i\hbar\dfrac{\partial\tilde\psi}{\partial t}=\left(\dfrac{1}{2m}(-i\hbar\nabla-\vec A)^2+\Lambda(\vec r)\right)\tilde\psi
$$
这里 $\vec A(\vec r)=i\hbar\,\mathcal U^\dagger(\vec r)(\nabla\mathcal U(\vec r))$ 。具体推导：
$$
\mathcal U^\dagger(-i\hbar\nabla)\mathcal U=-i\hbar\nabla-i\hbar\,\mathcal U^\dagger(\vec r)(\nabla\mathcal U(\vec r))
$$
 顺带一提，$\vec A$ 是一个实场。这是一个在Berry相位中用到的trick的结果。因为
$$
\mathcal U^\dagger(\vec r)(\nabla\mathcal U(\vec r))+(\nabla\mathcal U^\dagger(\vec r))\mathcal U(\vec r)=\nabla(\mathcal U^\dagger\mathcal U)=0
$$
因此 $\mathcal U^\dagger(\vec r)(\nabla\mathcal U(\vec r))$ 的实部为零。观察运动方程的形式，可以看到 $\vec A$ 实际上就是一个规范场。但与一般磁场产生的矢势场不同，$\vec A$ 是一个矩阵场。因此不同点的 $\vec A$ 一般不可交换，因此这是一个**非阿贝尔规范场**。$\vec A$ 的非对角项耦合了不同点处的自旋态，导致原子存在自旋态跃迁的可能。
但是，对于磁场缓变的情形，我们可以忽略那些非对角项，从而将 $\vec A$ 退化为对角的**阿贝尔规范场**。此时可以等效的定义**合成磁场**：
$$
\vec B_{syn}=\nabla\times\vec A_{ii}(\vec r)
$$
自旋态不会发生跃迁，因此我们可以将原子视为无自旋的。这时，我们发现一个有自旋的中性原子在磁场 $\vec B$ 中的运动，可以等效为带电粒子在合成磁场 $\vec B_{syn}$ 中的运动。由于后者有Aharonov-Bohm效应，可以推断前者中的中性原子沿一闭合路径运动时，同样会产生一个额外相位，相位与自旋沿轨迹形成的立体角成正比。
当然，当磁场快速变化时，上面的绝热近似失效，原子可以在不同自旋态间跃迁。因此，"low-field seeking"可能转变为"high-field seeking"，这称为**Majorana相变**。当相变发生时，原子将无法被磁阱捕获。这正是1995年前在磁阱中实现玻色-爱因斯坦凝聚态面临的主要挑战之一。

## 1.3 光位移

### AC Stark Shift

在光场下，原子会感受到一个等效势。这里我们以碱金属的基态为例。考虑基态 $^2S_{1/2}$ 与 $L=1$ 的激发态 $^2P_{3/2},^2P_{1/2}$。记两者能级差为 $E_{ex}\,(\sim\,\mathrm{eV})$，其主要与可见光能量匹配。记失谐为 $\Delta_e=E_{ex}-\hbar\omega$，其中 $\omega$ 是激光频率，一般而言失谐 $\Delta_e$ 大致与精细结构相当，而对于其他激发态，失谐都很大，因此我们可以只考虑这三个态，且超精细结构与Zeeman效应可忽略。如下图所示：

 <div align="center">
  <img src="Pasted image 20251217110705.png" width="250">
</div>

此模型的哈密顿量为：
$$
\hat H=\hat H_{at}+\hat H_d
$$
$\hat H_{at}$ 为原子部分的哈密顿量。
$$
\hat H_{at}=E_{ex}\mathcal P_e+\alpha_f\hat S\cdot\hat L
$$
其中 $\mathcal P_e$ 代表到激发态的**投影算符**，而 $\mathcal P_g$ 则代表到基态的投影算符。注意 $\hat H_{at}$ 不会耦合基态与激发态。  
激光带来的额外哈密顿量主要是电偶极项：
$$
\hat H_d=\vec d\cdot\vec E=\sum_{j=x,y,z}d_jE_j^0\cos(\phi_j-\omega t)
$$
考虑**旋波近似**，其引入下面的含时幺正变换：
$$
\mathcal U(t)=\mathrm{e}^{-i\omega t\mathcal P_e}=\mathcal P_g+\mathcal P_e\,\mathrm{e}^{-i\omega t}
$$
这实际上诱导了绘景变换。哈密顿量变为：
$$
\hat H_d\to\mathcal U^\dagger\hat H_d\mathcal U+i\hbar(\partial_t\mathcal U^\dagger)\mathcal U\approx\dfrac12\sum_{j=x,y,z}\left(\mathcal E_j^*\mathcal P_gd_j\mathcal P_e+\mathcal E_j^*\mathcal P_ed_j\mathcal P_g \right)
$$
别被吓到了，这只是代表了非对角项，其中 $\mathcal E_j=E_j^{(0)}\,\mathrm{e}^{i\phi_j}$。计算时注意 $\mathcal P_gd_j\mathcal P_g=\mathcal P_ed_j\mathcal P_e=0$。同时，$\hat H_{at}$ 变为：
$$
\hat H_{at}\to\mathcal U^\dagger\hat H_{at}\mathcal U+i\hbar(\partial_t\mathcal U^\dagger)\mathcal U=\Delta_e \mathcal P_e+\alpha_f\hat S\cdot\hat L
$$
$\Delta_e=E_{ex}-\hbar\omega$ 为前面提到的失谐，其中 $\Delta_e>0$ 称为**红失谐**，  $\Delta_e<0$ 称为**蓝失谐**。注意此时的Hamiltonian不含时，因此我们可以谈论其能量本征值。新的哈密顿量相当于把原来的基态能量向上提了一个 $\hbar\omega$。对于红失谐，此时的基态仍在激发态下，由于能级排斥，基态能量会下降，激发态能量会上升。而对于蓝失谐则会反过来。如下图所示：

 <div align="center">
  <img src="Pasted image 20251217134455.png" width="500">
</div>

旋波近似的物理意义：我们可将激光场量子化，其状态 $|N\rangle$ 用光子数标记。在二次量子化的形式下，$\vec d\cdot\vec E$ 耦合基态与激发态可以视为产生或湮灭一个光子。从状态 $|g\rangle|N\rangle$ 开始，原子可以先吸收一个光子到中间态 $|e\rangle|N-1\rangle$，再发射光子回到 $|g\rangle|N\rangle$ 。此时中间态的能量为 $\Delta_e$。但原子也可以通过发射光子到中间态 $|e\rangle|N+1\rangle$，再吸收光子回到 $|g\rangle|N\rangle$ ，此时中间态的能量为 $E_{ex}+\hbar\omega$。后者中间态的能量很高，因此发生概率显著降低，旋波近似正是忽略第二种过程。
上面这一在光场中，由于电偶极跃迁造成的能级移动便称为**交流斯塔克能移效应**(AC Stark Shift)。接下来，我们可以对其做一些更形式化的分析。
由于与电场作用项 $\hat H_d$ 的存在，基态的能量发生移动，利用二阶微扰公式，我们可以得到等效的哈密顿量为：
$$
\hat H_{eff}=-\mathcal P_g\hat H_d\mathcal P_e\hat H_{at}^{-1}\mathcal P_e\hat H_d\mathcal P_g
$$
你可能没见过这个形式，但是它实际上就是：
$$
E^{(2)}_g=\dfrac{|\langle g|\hat H_d|e\rangle|^2}{E_{ex}-E_g}
$$
请自行验证。我们进一步将其写为：
$$
\hat H_{eff}=-\dfrac14\sum_{i,j=x,y,z}\mathcal E_i^*\hat{\mathcal D}_{ij}\mathcal E_j,\quad \hat{\mathcal D}_{ij}=\mathcal P_g d_i\mathcal P_e\hat H_{at}^{-1}\mathcal P_ed_j\mathcal P_g
$$
$\hat{\mathcal D}_{ij}$ 是二阶Cartesian张量算子。下面来讨论 $\hat{\mathcal D}_{ij}$ 在不同情境下的特性。

### The Scalar Light Shift

首先我们考虑 $\alpha_f=0$ 的情形，也就是暂时忽略精细结构。则
$$
\hat{\mathcal D}_{ij}=\dfrac{1}{\Delta_e}\mathcal P_g d_id_j\mathcal P_g
$$
基态为 $L=0$ ，利用宇称，我们注意到只有当 $i=j$ 时 $d_id_j$ 在基态上的矩阵元才不是零。我们可以写出：
$$
\hat{\mathcal D}_{ij}=-4u_s\delta_{ij},\quad u_s=-\dfrac{e^2}{12\Delta_e}\langle g|r^2|g\rangle,\quad \hat H_{eff}=u_s\mathcal E^2
$$
其显然不能改变基态的自旋态，因为无精细结构下自旋与空间角动量解耦。因此，该项被称为**标量光移**(scalar light shift)，而 $u_s$ 称为原子的**标量光极化率**。
### 用激光捕获原子

激光可以捕获原子的关键便在于AC Stark Shift。注意到上面的标量势仅依赖于激光的强度，对于红失谐而言，$u_s<0$，因此原子会被束缚在激光强度的**局域极大值**处。这也可以由红失谐下基态能量下降看出。因此，通过聚焦激光束即可实现原子捕获，这正是激光捕获的基本原理。
另一个需要我们注意的点是我们忽略了从激发态到基态的**自发辐射**过程。我们可以通过向激发态能量中添加虚部来代表这一过程，此时
$$
u_s\propto\dfrac{1}{\Delta_e-i\varGamma}=\dfrac{\Delta_e}{\Delta_e^2+\varGamma^2}+i\dfrac{\varGamma}{\Delta_e^2+\varGamma^2}
$$
在非共振条件 $\Delta_e\gg \varGamma$ 下，实部与虚部近似是 $1/\Delta_e$ 与 $\varGamma/\Delta_e^2$。在远失谐区域，虚部相较于实部会被显著抑制。由于实部提供了捕获效应，激光捕获技术通常在远失谐区域进行。该技术于2018年荣获诺贝尔奖。

### 光晶格

考虑两束向相反方向传播的同频率激光，其会形成驻波，有
$$
\mathcal E_y=E^0\mathrm{e}^{ikx}+E^0\mathrm{e}^{-ikx}=2E^0\cos(kx)
$$
由于标量光移与电场强度成正比，因此这会形成周期势场：
$$
V(x)\propto\cos^2(kx)
$$
此即为**光晶格**(optical lattice)。

### 激光制冷

当失谐 $\Delta_e$ 变小时，标量势的**虚部**也会变得显著，这意味着**自发辐射过程**的重要性也随之提升。
受激辐射与自发辐射存在本质区别：在受激辐射中，由于光子的吸收与发射过程完全相同，动量传递会相互抵消，原子在经历整个二级过程后不会获得额外动量。而在自发辐射中，由于光子在发射过程中可朝任意方向传播，平均而言动量传递会被完全抵消，因此原子在吸收光子时会**受到激光场光子的推动**。
现在考虑两束向相反方向传播的激光，对于静止的原子，其受到左右激光的推动力互相抵消。但是对于一个比如向右运动的原子，由于Doppler效应，其会受到向左的反作用力。可以证明，激光对原子的作用力总是与原子的运动方向相反，因此会使其减速，从而达到**制冷**的效果。这就是**激光制冷**的基本原理。该技术是实现原子冷却至量子简并态的关键步骤之一。激光冷却技术因取得重大突破，于1997年荣获诺贝尔物理学奖。
然而，由于存在诸多限制，通过激光冷却直接实现原子气体的量子简并状态极为困难。在大多数实验中，需要在激光冷却后进行**蒸发冷却**。蒸发冷却的基本原理为：考虑深度为 $U_0$ 的有限深捕获势阱，对于那些动能大于 $U_0$ 的原子，它们会直接逃出势阱。此时若逐步降低 $U_0$，动能更大的原子会不断逃逸，剩余原子的平均动能随之降低，从而导致原子气体温度下降。
但需注意的是，**蒸发冷却**会以**损失原子**为代价来降低温度。当原子流失时，**简并温度也会随之下降**。因此，蒸发冷却的效率至关重要。降温速度必须快于简并温度的降低速度，否则系统永远无法达到量子简并状态。

## 1.4 Stimulated Raman Adiabatic Passage (STIRAP)

在1.3节中，我们讨论了原子在基态时可能通过双光子过程经由中间激发态产生有效势能。本节将探讨一种动态过程，该过程同样通过双光子过程经由中间态实现原子从一个低能态到另一个低能态的跃迁，这一过程被称为**受激拉曼绝热路径**（STIRAP）。
对于一个最简单的模型，考虑两个能量为 $E_1,E_2$ 的低能态 $|1\rangle,|2\rangle$，以及一个能量为 $E_{ex}$ 的激发态 $|e\rangle$ 。一个称为“泵浦激光器”的激光器用频率为 $\omega_p$ 的激光将$|1\rangle,|e\rangle$ 耦合，其强度由Rabi频率 $\Omega_p(t)$ 刻画。另一个称为“Stokes激光器”的激光器用频率为 $\omega_s$ 的激光将$|2\rangle,|e\rangle$ 耦合，其强度由 $\Omega_s(t)$ 刻画。定义两个失谐：
$$
\Delta_p=E_{ex}-E_1-\hbar\omega_p,\quad \Delta_s=E_{ex}-E_2-\hbar\omega_s
$$
STIEAP要求 $\Delta_p=\Delta_s$，下面将用 $\Delta$ 表示。在旋波近似下，此时的哈密顿量表示为：
$$
\hat H(t)=\hbar|\psi\rangle\mathcal H(t)\langle\psi|^T,\quad \mathcal H(t)=\begin{pmatrix}
0&0&\Omega_p(t)\\
0&0&\Omega_s(t)\\
\Omega_p(t)&\Omega_s(t)&\Delta
\end{pmatrix}
$$
其中 $|\psi\rangle=(|1\rangle,|2\rangle,|e\rangle)$。哈密顿量可以写为：
$$
\hat H(t)=A(t)\left[\left(\dfrac{\Omega_p(t)}{A(t)}|1\rangle+\dfrac{\Omega_s(t)}{A(t)}|2\rangle\right)\langle e|+h.c.\right]+\Delta|e\rangle\langle e|
$$
其中 $A(t)=\sqrt{\Omega_p^2(t)+\Omega_s^2(t)}$。现在定义一个“**亮态**”。
$$
|B\rangle=\dfrac{\Omega_p(t)}{A(t)}|1\rangle+\dfrac{\Omega_s(t)}{A(t)}|2\rangle
$$
另一个“**暗态**”定义为：
$$
|D\rangle=-\dfrac{\Omega_s(t)}{A(t)}|1\rangle+\dfrac{\Omega_p(t)}{A(t)}|2\rangle
$$
即在 $\{|1\rangle,|2\rangle\}$ 张成的二维Hilbert空间中重新取了一组基 $\{|B\rangle,|D\rangle\}$。此时的Hamiltonian为：
$$
\hat H(t)=A(t)\left[|B\rangle\langle e|+h.c.\right]+\Delta|e\rangle\langle e|
$$
可以看到，在Hamitonian中不会出现暗态，只有亮态与激发态 $|e\rangle$ 耦合。换言之，对于任意给定时间 $t$，$\mathcal H(t)$ 均可通过酉矩阵 $\mathcal U(t)$ 对角化，且总存在瞬时本征态 $|D(t)\rangle$，其本征能量**始终为零**。另外两个瞬时本征态将处于 $|B\rangle$ 与 $|e\rangle$ 的叠加态，其能量为 $\pm\sqrt{A^2(t)+\Delta^2/4}$。

 <div align="center">
  <img src="Pasted image 20251217144235.png" width="600">
</div>

STIEAP的关键便在于这个**暗态** $|D(t)\rangle$。当我们绝热的改变 $\Omega_p(t),\Omega_s(t)$ 时，系统可以维持在一个瞬时能量本征态上（绝热定理）。对于 STIRAP 而言，我们希望系统始终维持在暗态 $|D(t)\rangle$ 中。为实现这一目标，初始时 $\Omega_p/\Omega_s\to 0$，因此 $|D\rangle\to|1\rangle$；而最终 $\Omega_s/\Omega_p\to 0$，因此 $|D\rangle\to|2\rangle$。具体的步骤如上图所示，其分为三个阶段：
1. 初始阶段，原子占据 $|1\rangle$ 态，首先开启 $|2\rangle$ 与 $|e\rangle$ 间的耦合 $\Omega_s(t)$。
2. 中间阶段，两个激光器的耦合均开启，原子从 $|1\rangle$ 态转移到 $|2\rangle$ 态。
3. 当原子逐渐转移至 $|2\rangle$ 态时，$|e\rangle$与较少占据的 $|1\rangle$ 态之间的耦合应保持开启。
这样的绝热变化可以使体系始终待在暗态 $|D\rangle$ 上，从而完成从 $|1\rangle$ 态到 $|2\rangle$ 态的转移。STIEAP有下面两个主要优势：
- 激发态 $|e\rangle$ 上始终没有原子，从而避免了**自发辐射**的问题。
- 此方案对 $\Omega_p(t)$ 与 $\Omega_s(t)$ 的具体分布不敏感，只需要满足前述的**初始条件**（即打开与关闭顺序）以及**绝热条件**即可。
STIRAP 技术在原子分子物理学及化学领域应用广泛。在冷原子物理研究中，该技术主要用于制备**超冷基态分子**。

 <div align="center">
  <img src="Pasted image 20251217154752.png" width="500">
</div>
---
