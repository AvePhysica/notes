## 2.1 散射长度

粒子间的**相互作用**在量子多体物理中扮演了重要的角色。超冷原子物理研究的是中性原子的稀薄气体，而凝聚态物理则主要聚焦于固体中的电子气体。这两个体系中多体现象的诸多根本差异，都可以追溯到它们粒子间相互作用形式的不同。电子间的相互作用表现为库仑排斥，原子间的势能则包含吸引性的范德华力和极短距离下的强排斥作用。超冷原子间的这种相互作用具有以下三个关键特征，这些特征对后续讨论至关重要。
- **短程**。范德瓦尔斯相互作用 $V(\vec r)$ 是短程的，我们可以假设 $r_0$ 为其**力程范围**，认为当 $r>r_0$ 时 $V(\vec r)\simeq 0$。
- **稀薄**。超冷原子气体是极其稀薄的，其分子间距 $d$ 远大于 $r_0$。
- **低能**。超冷原子的温度极低，因此其热运动能量也是极小的。而分子间相互作用势能大致为 $\hbar^2/(mr_0^2)$，因此此条件可以表示为 $kr_0\ll 1$，其中 $k=2\pi/\lambda$ 为热运动对应的波矢。
在这三个条件下，我们会觉得原子间本来的距离就大，能量低又导致其根本不可能彼此接近，故大多数情况下任意两个原子之间的距离都**远大于**相互作用势能为零的阈值。因此，经典力学中原子之间不会产生任何相互作用力，此时气体呈现为**非相互作用体系**。然而，正如本章将要展示的，在量子力学框架下，该体系不仅会形成相互作用，有时甚至会演变为强相互作用体系。其来源为量子散射理论中的**相移**(phase shift)。
### 相移

我们来复习一下**低能散射**的相关内容。在两体散射的相互作用势为 $V(\vec r)$ 时，定态薛定谔方程写为：
$$
\left[-\dfrac{\hbar^2}{2\bar m}\nabla^2+V(\vec r)\right]\psi(\vec r)=E\psi(\vec r)
$$
这里 $\bar m=m/2$ 代表约化质量，$\vec r$ 代表两个原子的相对径矢。我们可以将波函数在**角动量本征基**下展开，这称为**分波**：
$$
\psi(\vec r)=\sum_{l=0}^\infty\dfrac{\chi_{kl}(r)}{kr}P_l(\cos\theta)
$$
在中心对称的势场（即仅依赖于距离 $r$）$V(r)$ 中，每个分波之间是**解耦**的，每个分波的径向部分满足下面的径向薛定谔方程：
$$
\dfrac{\mathrm{d}^2\chi_{kl}}{\mathrm{d}r^2}-\dfrac{l(l+1)}{r^2}\chi_{kl}+\dfrac{2\bar m}{\hbar^2}(E-V(\vec r))\chi_{kl}=0
$$
不同分波对应的第二项离心势不同。在低能散射下，离心势会阻碍粒子的进入，因此越高分波的贡献越小，具体来说是呈现出一个**阈行为**(threshold behavior)：
$$
\delta_{kl}\propto k^{2l+1}
$$
具体证明参见[[散射理论 Part.IV 低能散射与高能散射]]。因此我们可以先考虑贡献最大的 $s$ 分波。在力程范围 $r_0$ 之外，其呈现出三角函数形式：
$$
\chi^s_k=A\sin(kr+\delta_k)
$$
这里 $\delta_k$ 即为 $s$ 分波的**相移**。其由势场边界上的波函数及其导数连续的边界条件确定，因此势场的确可以影响到势场外部的波函数。边界条件为：
$$
\dfrac{\chi'(r>r_0)}{\chi(r>r_0)}\bigg|_{r>r_0}=\dfrac{k\cos(kr_0+\delta_k)}{\sin(kr_0+\delta_k)}\simeq\dfrac{k}{\tan\delta_k}=\dfrac{\chi'(r>r_0)}{\chi(r>r_0)}\bigg|_{r<r_0}
$$
这里用到了低能散射条件 $kr_0\ll 1$。现在，我们希望寻求一个能整体刻画势场的物理量。可以发现，实际上影响相移的只是势场边界上波函数的对数微商，受此启发，我们直接定义：
$$
\dfrac{k}{\tan\delta_k}=\dfrac{\chi'(r>r_0)}{\chi(r>r_0)}\bigg|_{r<r_0}\equiv-\dfrac{1}{a_s}
$$
$a_s$ 称为（$s$ 分波的）**散射长度**。这样，不论我们的势场具有怎样的形式，决定外部相移 $\delta_k$ 的都是其散射长度：
$$
\tan\delta_k=-ka_s
$$
由于正切函数的周期性，我们一般限制 $\delta_k\in[-\pi/2,\pi/2]$，则散射长度事实上可以取一切实数值。

>[!add]
>上面我们应用低能条件，直接忽略了 $kr_0$。这可能会有些不妥，为了保险起见，我们还是将其影响保留到一阶：
>$$\tan(kr_0+\delta_k)\approx\tan\delta_k+\dfrac{kr_0}{\cos^2\delta_k}=-ka_s$$
>得到
>$$\tan\delta_k=-ka_s-(1+k^2a_s^2)kr_0\equiv-ka_s-\dfrac12 r_{\mathrm{eff}}\,a_s^2k^2$$
>这里 $r_{\mathrm{eff}}$ 称为有效长度，一般而言，这一项的影响在低能散射中可忽略不计，但也有一些特例，比如当 $a_s\to 0$ 时 $kr_0\ll \delta_k$ 就不一定成立，这时我们原先的近似就不一定合适了。此时 $\tan\delta_k$ 不与 $k$ 成线性关系，而是与 $k^3$ 成线性关系。

散射长度有一个很明确的物理意义。考虑 $r>r_0$ 的外部区域，在低能近似下，波函数近似为：
$$
\chi^s_k\propto\sin(kr+\delta_k)\simeq\sin\delta_k+\cos\delta_k\,(kr)\propto1+\dfrac{k}{\tan\delta_k}r=1-\dfrac{r}{a_s}
$$
可以看到其近似为一条直线，而 $x$ 轴的截距即为散射长度 $a_s$。当然，这是近似的结果，此结果在所谓的**零能散射**下是严格的。关于零能散射也可参见[[散射理论 Part.IV 低能散射与高能散射]]。这里放一张方势阱散射的示意图：

 <div align="center">
  <img src="Pasted image 20251218143721.png" width="600">
</div>

可以看到，散射长度 $a_s$ 与势场尺度 $r_0$ 并无直接的关系，当势阱深度逐渐变化时，散射长度也从 $-\infty$ 到 $+\infty$ 周期性变化，相应的相移 $\delta_k$ 也在 $[-\pi/2,\pi/2]$ 间周期性变化。

### **浅的**束缚态

现在，我们暂时转向束缚态，当能量 $E<0$ 时，此时外部 $r>r_0$ 区域的方程为：
$$
\dfrac{\mathrm{d}^2\chi}{\mathrm{d}r^2}+\dfrac{2\bar m E}{\hbar^2}\chi=0
$$
其解为：
$$
\chi=A\exp\left(-\sqrt{\dfrac{2m|E|}{\hbar^2}}\,r\right)
$$
我们舍掉了正的指数项，因为其于无穷远处发散。注意：对于散射态，方程的解 $\cos(kr),\sin(kr)$ 都是可取的，因此这一个额外的自由度放到了相移 $\delta_l$ 上，因此我们可以通过边界条件确定相移。而对于束缚态，我们只能取负的指数项，这样边界条件将确定能量：
$$
\dfrac{\chi'}{\chi}\bigg|_{r=r_0}=-\sqrt{\dfrac{2\bar m |E|}{\hbar^2}}=-\dfrac{1}{a_s}
$$
解得
$$
E_b=-\dfrac{\hbar^2}{2\bar ma_s^2}
$$
因此束缚态的能量同样由散射长度唯一确定。要注意的是，仅当 $a_s>0$ 时才会存在束缚态。

>[!tip]
>看到这里，你可能有一些疑惑。对于一个吸引势，比如一个方势阱，怎么看它都不止一个束缚态吧。那为什么我们上面求出的束缚态是唯一的呢？
>这是由于我们采取的是低能散射近似，对于那些更深的束缚态，其根本就不满足低能条件，因此不会出现在我们的解中，我们解出的是**最浅的**那个束缚态。当 $a_s$ 从正变负时，正是最浅的束缚态能量逐渐上升，最终消失的过程。

现在，我们可以画出下面随势阱深度增加，散射长度与束缚态能量的变化曲线：

 <div align="center">
  <img src="Pasted image 20251218151527.png" width="500">
</div>

可以看到，当散射长度 $a_s$ 的符号由负变正时，下面的三件事会在此点发生：
- $s$ 波的散射长度由 $-\infty$ 跳到 $+\infty$。
- 相移由 $-\pi/2$ 跳到 $+\pi/2$。
- 出现束缚态。
这一点被称为**散射共振**(scattering resonance)。实际上，相移的突变与零能束缚态的出现相联系有更深刻的物理内涵，这被称为Levinson定理。这里就不展开了。

### 散射振幅

最后，我们来讨论一下散射振幅的问题。总的散射振幅 $f(\theta)$ 定义为：
$$
\psi=\mathrm{e}^{ikz}+f(\theta)\dfrac{\mathrm{e}^{ikr}}{r}
$$
而分波散射振幅 $f_l(k)$ 定义为：
$$
f(\theta)=\sum_{l=0}^{+\infty}(2l+1)f_l(k)P_l(\cos\theta)
$$
参考[[散射理论 Part.III 角动量表象：分波与相移]]中的推导，可以得到
$$
f_s=\dfrac{\mathrm{e}^{2i\delta}-1}{2ik}=-\dfrac{1}{1/a_s+ik}
$$
其同样由散射长度确定。而对应分波的总截面为：
$$
\sigma_s=4\pi|f_s|^2=\dfrac{4\pi}{k^2}(2l+1)\sin^2\delta_k
$$
- 当 $ka_s\ll 1$ 时，$\sigma_s=4\pi a_s^2$。这是对应于零能散射的严格散射截面。
- 当 $ka_s\gg 1$ 时，$\sigma_s=\dfrac{4\pi}{k^2}$ 。这一区域称为**幺正区域**(unitary regime)。其仅取决于粒子的热运动动量，而不取决于势场的具体形式。
### 硬球散射的启发

硬球散射是一个典型的短程排斥势情形。其相移为：
$$
\delta_s=-kR_0
$$
现在，假设原子间具有吸引势，但是其散射长度仍然可以取任何值，因此也有可能取到上面的 $-kR_0$。因此，对于一个范围内的小 $k$，当散射长度 $a_s>0$ 时，其相移将等价于一个硬球排斥势下的相移。
但这是有条件的：
1. $ka_s\ll 1$ 且仅考虑低能散射。
2. 束缚态足够深使得我们可以忽略其影响。
因此并不是所有正的 $a_s$ 都代表排斥势。

## 2.2 零程作用模型

我们已经讨论了当相互作用势限制在一个有限范围内时，两体低能散射呈现出的行为。本节我们希望建立一个有效模型以描述多体系统中的相互作用效应，并要求该有效模型具备以下两个特征：
- 在有效模型中仅使用 $s$ 波**散射长度** $a_s$ 作为唯一参数，并忽略原子间势的微观细节。
- 为便于后续多体理论研究，该有效模型采用**零程近似**（即两个原子仅在完全处于同一空间位置时相互作用）。在第2.1节中，我们始终将相互作用范围 $r_0$ 设为有限值，而在本节中，应将 $r_0$ 趋近于零。
下面我们介绍两种有效的模型，其均可给出相同的散射长度。
### 赝势(Pseudopotential)

最简单的零程作用即为delta函数，即 $V(\vec r)\propto\delta(\vec r)$。我们记 $V(\vec r)=\delta(\vec r)\hat O(r)$。定态薛定谔方程为：
$$
\left[-\dfrac{\hbar^2}{2\bar m}\nabla^2+V(\vec r)\right]\psi(\vec r)=E\psi(\vec r)
$$
其解为
$$
\psi(r)=\dfrac{\sin(kr+\delta_k)}{kr},\quad r\ne 0
$$
我们在 $r=0$ 附近将其展开：
$$
\psi(r)=\dfrac{1}{r}-\dfrac{1}{a_s}+o(kr)
$$
可以发现
$$
[\partial_r\cdot r]\psi(r)=-\dfrac{1}{a_s}+o(kr)
$$
现在我们定义：
$$
\hat O(r)=\dfrac{2\pi\hbar^2a_s}{\bar m}\partial_r\cdot r\Rightarrow V(\vec r)\psi(r)=-\dfrac{2\pi^2\hbar^2}{\bar m}\delta(\vec r)
$$
因此此时薛定谔方程为：
$$
-\dfrac{\hbar^2}{2\bar m}\nabla^2\psi(r)=\dfrac{2\pi\hbar^2}{\bar m}\delta(\vec r)
$$
代入波函数的具体形式，可以验证上式的确是正确的。因此我们选取的势 $V(\vec r)=\delta(\vec r)\hat O(r)$ 的确给出了相同的散射长度。这称为**Fermi赝势法**。

## 可重整化的相互作用势

Fermi赝势的确可以作为一种等效接触势，但其缺陷在于算符不具备厄米特性。因此在诸多场景下使用该模型并不便利。对于多体物理研究，采用delta函数形式的接触势 $V(\vec r)=g\delta(\vec r)$ 仍不失为便捷选择。尽管我们已知该模型在短程距离会产生发散问题。此时二次量子化形式下的Hamiltonian为
$$
\hat H=\int\mathrm{d}^3\vec r\,\hat\psi^\dagger(\vec r)\left[-\dfrac{\hbar^2}{2m}\nabla^2\right]\hat\psi(\vec r)+g\int\mathrm{d}^3\vec r\,\mathrm{d}^3\vec r'\,\hat \psi^\dagger(\vec r)\hat\psi^\dagger(\vec r')\hat\psi(\vec r')\hat\psi(\vec r)
$$
首先，将其换到动量空间（Fourier变换）：
$$
\hat H=\sum_{\vec k}\dfrac{\hbar^2k^2}{2m}\hat\psi_k^\dagger\hat \psi_k+\dfrac{g}V\sum_{\vec k,\vec k_1,\vec k_2}\hat \psi^\dagger_{k/2+k_1}\hat\psi^\dagger_{k/2-k_1}\hat\psi_{k/2-k_2}\hat\psi_{k/2+k_2}
$$
其跃迁矩阵的Feynman图为：

 <div align="center">
  <img src="Pasted image 20251219083521.png" width="500">
</div>

这实际上就是**Schwinger–Dyson方程**：
$$
T_2(E)=g+\dfrac{g}{V}\sum_{\vec p}\dfrac{1}{E-\hbar^2\vec p^2/m+i0^+}T_2(E)=g+\dfrac{g}{V}\sum_{\vec p}\dfrac{1}{E-\hbar^2\vec p^2/m+i0^+}g+\cdots
$$
即
$$
T_2(E)=\dfrac{g}{1-\dfrac{g}{V}\displaystyle\sum_{\vec p}\dfrac{1}{E-\hbar^2\vec p^2/m+i0^+}}
$$
然而，这个求和是发散的，在大的 $\vec p$ 下，有
$$
\sum_{\vec p}\dfrac{1}{E-\hbar^2\vec p^2/m+i0^+}=\int\mathrm{d}^3\vec p\dfrac{1}{E-\hbar^2\vec p^2/m+i0^+}\sim\int\dfrac{\mathrm{d}^3\vec p}{p^2}\sim\int{\mathrm{d}p}\quad\text{is divergent}
$$
由于这是发生在大 $p$ 处的发散，其称为**紫外发散**(ultraviolet divergence)。这是个严重的问题，其来源便是我们简单假设势的形式是 $V(\vec r)=g\delta(\vec r)$。相互作用参数 $g$ 不是一个物理参数。我们需要找到恰当的重整化方法，将相互作用参数 $g$ 与物理参数建立关联。因此，让我们重新表述
$$
T_2(E)=\dfrac{g}{\displaystyle1-\dfrac{g}{V}\sum_{\vec p}\dfrac{1}{\hbar^2\vec p^2/m}-\dfrac{g}{V}\sum_{\vec p}\left(\dfrac{1}{E-\hbar^2\vec p^2/m+i0^+}-\dfrac{1}{\hbar^2\vec p^2/m}\right)}=\dfrac{1}{\displaystyle\dfrac{1}{g}+\dfrac 1V\sum_{\vec p}\dfrac{1}{\hbar^2\vec p^2/m}+\dfrac{ikm}{4\pi\hbar^2}}
$$
我们可以写出：
$$
T_2(E)=\dfrac{4\pi\hbar^2}{m}\dfrac{1}{1/a_s+ik}=\dfrac{1}{\displaystyle\dfrac{1}{g}+\dfrac 1V\sum_{\vec p}\dfrac{1}{\hbar^2\vec p^2/m}+\dfrac{ikm}{4\pi\hbar^2}}
$$
因此我们可以形式化的写出：
$$
\dfrac{m}{4\pi\hbar^2a_s}=\dfrac{1}{g}+\dfrac 1V\sum_{\vec p}\dfrac{1}{\hbar^2\vec p^2/m}
$$
也就是说 $g$ 实际上对后面的发散项做了**重整化**(Renormalization)，使得右侧整体回到我们的物理量散射长度 $a_s$ 上。
然而，这里存在一个关键问题：我们通过匹配二体散射振幅获得了重整化条件，但如何确保该条件适用于多于两个粒子的系统？一般而言，答案是存在可能性——若成立则称为**可重整化**理论；若不成立，则意味着在少体或多体系统中会出现额外的高能标度，这些标度具有重要影响。

## 2.3 依赖于自旋的相互作用

事实上，原子自旋在双体碰撞中扮演着至关重要的角色，其作用在**零磁场极限**与**有限磁场**区域存在显著差异。在零磁场极限下，自旋旋转对称性得以保持，这种对称性对双体相互作用的形式施加了约束条件，相关内容将在本节展开讨论。而在有限磁场区域，自旋旋转对称性因塞曼能而被破坏，但自旋的塞曼能可作为调控双体相互作用的工具，具体讨论将在第2.4节进行。

### 碱金属原子

考虑两个自旋为 $f$ 的碱金属原子的碰撞，这里 $f$ 是指总超精细自旋。简单起见，我们假设 $f=1$。由于自旋旋转对称性，碰撞的末态总自旋为 $F=0,1,2$，相互作用势可以写为：
$$
\hat V(\vec r)=\dfrac{2\pi\hbar^2}{\bar m}(a_0\mathcal P_0+a_2\mathcal P_2)\delta(\vec r)\partial_r\cdot r
$$
这里 $a_0$ 与 $a_2$ 指 $F=0$ 与 $F=2$ 的散射通道的散射长度，这里没有 $F=1$ 通道的原因是其为**反对称**的，因此该通道中 $s$ 波散射被禁戒。$\mathcal P_F$ 指到总角动量 $F$ 的子空间的投影算符。我们可以用两个角动量的点乘 $\vec f_1\cdot\vec f_2$ 来表示投影算符：
$$
\vec f_1\cdot\vec f_2=\dfrac12(\vec F^2-\vec f_1^2-\vec f_2^2)=\sum_F\left(\dfrac{F(F+1)}{2}-f(f+1)\right)\mathcal P_F
$$
因此
$$
\mathcal P_0+\mathcal P_2=1,\quad -2\mathcal P_0+\mathcal P_2=\vec f_1\cdot\vec f_2
$$
因此相互作用势可以表示为：
$$
\hat V(\vec r)=\dfrac{2\pi\hbar^2}{\bar m}\left(a^{(n)}+a^{(s)}\vec f_1\cdot\vec f_2\right)\delta(\vec r)\partial_r\cdot r
$$
其中
$$
a^{(n)}=\dfrac{a_0+2a_2}{3},\quad a^{(s)}=\dfrac{a_2-a_0}{3}
$$
这里的 $n,s$ 分别代表**密度相关**的相互作用以及**自旋相关**的相互作用。当 $a_0=a_2$ 时，其代表着散射与自旋无关，因此 $a^{(s)}=0$ ，这正是我们期望的结果。此时，相互作用仅依赖于总密度，总系统具有 $SU(3)$ 对称性。这是由于系统散射完全不依赖于自旋，而 $f=1$ 的自旋空间是三维复空间，我们可以对此空间进行任意的幺正变换，变换全体自然构成 $SU(3)$。另一方面，当 $a_0\ne a_2$ 时，变换不能混合不同的总角动量空间，因此系统实际上具有 $SU(2)$ 对称性，每一个 $F$ 对应的角动量空间都是 $SU(2)$ 的一个不可约表示空间。
实际上，对于 $^{87}\mathrm{Rb}$ 和 $^{23}\mathrm{Na}$ 等原子而言，$a_0$ 与 $a_2$ 之间的差异实际上非常微小。然而 $a^{(s)}$ 仍在碱金属散射中扮演重要角色，因为其中含有 $f_1^+f_2^-+f_1^-f_2^+$，因此这一项使得原子的**自旋态**可以发生改变。这一现象已在实验中被观测到。

### 碱土金属元素

对于基态而言，碱土金属原子的自旋完全属于核自旋 $I$。核自旋仅在**费米型**碱土金属原子中非零。由于核自旋与电子自由度之间的**解耦**，两个基态碱土金属原子之间的相互作用几乎与核自旋 $I$ 无关。因此，任意两个组分之间的散射长度完全相同，相互作用仅取决于总密度。这种相互作用项具有 $SU(2I+1)$ 对称性。
碱土金属的另一特性在于基态 $^1S_0$ 与时钟态 $^3P_0$ 间的散射。将这两个态记为 $|g\rangle$ 与 $|e\rangle$，同时将涉及到的两个核自旋态记为 $|\uparrow\rangle,|\downarrow\rangle$。由于 $s$ 波散射要求空间波函数是对称的，同时总波函数要是反对称的，因此自旋的波函数一定是**反对称**的。再分为核自旋与电子自旋，有以下四种可能：
$$
\begin{align}
|+\rangle&=\dfrac{1}{2}(|g\rangle|e\rangle+|e\rangle|g\rangle)\otimes(|\!\uparrow\rangle|\!\downarrow\rangle-|\!\downarrow\rangle|\!\uparrow\rangle)\\
|-,0\rangle&=\dfrac{1}{2}(|g\rangle|e\rangle-|e\rangle|g\rangle)\otimes(|\!\uparrow\rangle|\!\downarrow\rangle+|\!\downarrow\rangle|\!\uparrow\rangle)\\
|-,1\rangle&=\dfrac{1}{\sqrt 2}(|g\rangle|e\rangle+|e\rangle|g\rangle)\otimes|\!\uparrow\rangle|\!\uparrow\rangle\\
|-,-1\rangle&=\dfrac{1}{\sqrt 2}(|g\rangle|e\rangle+|e\rangle|g\rangle)\otimes|\!\downarrow\rangle|\!\downarrow\rangle
\end{align}
$$
现在假设 $\mathcal P_{\pm}$ 为投影到 $|+\rangle$ 空间与三个 $|-\rangle$ 总空间的投影算符。相互作用可写为：
$$
\hat V(\vec r)=\dfrac{2\pi\hbar^2}{\bar m}(a_+\mathcal P_++a_-\mathcal P_-)\delta(\vec r)\partial_r\cdot r
$$
其中 $a_{\pm}$ 是两个不同的散射长度。因此，在碰撞过程中，两个不同轨道态之间的核自旋可发生交换。

## 2.4 Feshbach共振

散射长度是描述原子间相互作用的重要参数。那么，我们能否通过实验手段调节散射长度呢？在4.1节中，我们以方势阱为例，证明了通过改变方势阱的深度可以调节散射长度。然而在实际操作中，要在较宽的能量范围内调节范德华势的强度存在较大难度。这里，我们将讨论通过改变外磁场来调节散射长度的**Feshbach共振**。
关于磁性Feshbach共振的讨论涉及原子在磁场中的内部自旋结构。本节研究的是外部Zeeman磁场足够强的区域，其会破坏自旋旋转对称性。让我们看一个具体的例子：考虑两个碱金属间的相互作用，其磁场能级结构在[[Lecture 1. A Single Atom]]中的1.2节讨论过。记单个原子的自旋本征态为 $|q\rangle$ ，其有确定的量子数 $F_z$。当两个原子离得足够远时，其状态可以用直积态 $|q_1\rangle\otimes|q_2\rangle$ 描述。
现在，我们引入两个**散射通道**的概念，其分别称为**开通道**(open channel)与**闭通道**(close channel)。这两个通道定义为两个原子离得足够远时的本征态。现在有几个点需要注意：
- **量子数**：由于系统具有绕 $z$ 轴的旋转对称性，因此沿 $z$ 方向的总角动量 $F_z^1+F_z^2+L_z$ 守恒。对于 $s$ 波散射，有 $L_z=0$。因此开通道与闭通道的 $F_z^1+F_z^2$ 应当相等。例如，下图是 $^6\mathrm{Li}$ 的磁场能级结构（核自旋 $I=1$），取开通道为 $|a\rangle\otimes|b\rangle$，则 $F_z=0$，因此另外允许的四个通道为 $|a\rangle\otimes|d\rangle,|b\rangle\otimes|e\rangle,|d\rangle\otimes|e\rangle,|c\rangle\otimes|f\rangle$。

<div align="center">
  <img src="Pasted image 20251221104518.png" width="500">
</div>

- **开通道与闭通道**：当原子离得足够远时，闭通道与开通道的能量差可以直接从上图读出，一般而言，能量差是远高于低能散射的动能的。因此，当两个原子从开通道进行低能散射时，其无法被散射到闭通道的散射态中。当选取开通道为 $|a\rangle\otimes|b\rangle$ 时，上面四个通道都可以作为闭通道。
- **能量可调**：通过调节外磁场，我们可以改变开通道与闭通道的能量。增大磁场时会增加能级差，因此可以设想，随着磁场增强，散射阈值（动能）可能从上方趋近闭通道的束缚态能量。
- **通道间的耦合**：当两个原子彼此靠近时，它们之间的原子间势能主要取决于两者的电子自由度。由于每个碱金属原子都拥有一个电子，因此原子间势能取决于它们的总电子自旋是**单重态**还是**三重态**（在短程排斥部分存在自旋依赖）。以开通道 $|a\rangle\otimes|b\rangle$ 为例，在磁场的极化下，总电子自旋更接近于三重态。然而，由于**超精细结构**的存在，其会混合电子的三重态与单态。因此，我们可以说短程相互作用耦合了不同的通道。

### 通道耦合模型

我们可以采用简化的耦合通道模型来展示磁场如何改变散射长度，模型示意图：

<div align="center">
  <img src="Pasted image 20251221113048.png" width="800">
</div>

我们来进行一些分析：
 - 当原子距离 $r>r_0$ 时，开通道与闭通道**解耦**，记其为 $|o\rangle$ 与 $|c\rangle$。因为闭通道的能量远高于冷原子的典型动能，因此此区域中波函数全部位于开通道中，有
$$
\chi=\sin(kr+\delta_k)|o\rangle
$$
- 当 $r<r_0$ 时，相互作用使得两通道间发生**耦合**，此时的波函数在两个通道中均有分量，记
$$
\chi=\chi_+|+\rangle+\chi_-|-\rangle=(\chi_+\cos\theta+\chi_-\cos\theta)|c\rangle+(\chi_+\cos\theta+\chi_-\sin\theta)|o\rangle
$$
其中$|\pm\rangle$ 为两通道的叠加态：
$$
|+\rangle=\cos\theta\,|o\rangle+\sin\theta\,|c\rangle,\quad|-\rangle=-\sin\theta\,|o\rangle+\cos\theta\,|c\rangle
$$
这里的线性组合是为了使得相互作用在 $|\pm\rangle$ 下**对角化**。由于相互作用很弱，不失一般性的，我们可以假设 $\theta$ 不依赖于空间位置，且其始终很小。现在，考虑 $r=r_0$ 处的边界条件：
$$
\chi_+\sin\theta+\chi_-\cos\theta\,\big|_{r=r_0}=0,\quad \dfrac{\chi_+'\cos\theta-\chi_-'\sin\theta}{\chi_+\cos\theta-\chi_-\sin\theta}\bigg|_{r=r_0}=-\dfrac{1}{a_s}
$$
解得下面的关系：
$$
-\dfrac{1}{a_s}=\dfrac{\chi_+'}{\chi_+}\bigg|_{r=r_0}\cos^2\theta+\dfrac{\chi_-'}{\chi_-}\bigg|_{r=r_0}\sin^2\theta
$$
$|+\rangle$ 通道的散射长度是：
$$
\dfrac{\chi_+'}{\chi_+}\bigg|_{r=r_0}=-\dfrac{1}{a_{bg}}
$$
$a_{bg}$ 称为**背景散射长度**。一般来说，$\theta$ 很小，可以近似认为 $\cos^2\theta\approx 1,\sin^2\theta\approx\theta^2$，因此仅当 $\chi_-'/\chi_-|_{r=r_0}$ 很大时，第二项才会有可观的贡献。
我们考虑 $|-\rangle$ 通道，假设其等效于一个方势阱 $V(r)=-V_0,r<r_0$。当散射能量远小于势垒深度时，有 $\chi_-=\sin(q_1 r),q_1=\sqrt{mV_0/\hbar^2}$，因此：
$$
\dfrac{\chi_-'}{\chi_-}\bigg|_{r=r_0}=\dfrac{q_1\cos(q_1r_0)}{\sin(q_1r_0)}
$$
现在，再假设存在一个能量为 $E_c$ 的束缚态，则束缚态的波函数为 $\chi_-=\sin(q_2 r),q_2=\sqrt{m(V_0+E_c)/\hbar^2}$，且边界条件要求 $\sin(q_2r_0)=0$。由于束缚态能量一般在低能散射的动能量级，因此可以认为 $E_c$ 很小，我们可以在 $q_1=q_2$ 处展开：
$$
\dfrac{\chi_-'}{\chi_-}\bigg|_{r=r_0}\approx\dfrac{q_1}{(q_1-q_2)r_0}\approx\dfrac{2q_1^2}{(q_1^2-q_2^2)r_0}=-\dfrac{2\hbar^2q_1^2}{mr_0E_c}
$$
因此可以看到 $\chi_-'/\chi_-|_{r=r_0}$ 反比于 $E_c$ 。记 $\gamma=2\hbar^2q_1^2\theta^2/(mr_0)$，则总的散射长度为：
$$
\dfrac{1}{a_s}=\dfrac{1}{a_{bg}}+\dfrac{\gamma}{E_c}
$$
注意 $\gamma$ 依赖于 $\theta$ ，即依赖于两通道间的耦合强度。在存在磁场 $B$ 时，开通道与闭通道的散射阈值分别变化 $-\mu_oB$ 与 $-\mu_cB$，一般而言，$\mu=\mu_o-\mu_c>0$，此时 $E_c$ 被替换为 $E_c-\mu_cB+\mu_oB=E_c+\mu B$，因此散射长度为：
$$
a_s=a_{bg}\left(1+\dfrac{\gamma a_{bg}}{E_c+\mu B+\gamma a_{bg}}\right)=a_{bg}\left(1-\dfrac{\Delta}{B-B_{res}}\right),\quad \Delta=\dfrac{\gamma a_{bg}}{\mu},\quad B_{res}=-\mu^{-1}E_c-\Delta
$$
因此在Feshbach共振点处 $B=B_{res}$ 处，散射长度趋近于无限大。另一方面，在4.1节的讨论指出，对于一个很大的 $a_s>0$，会有一个**弱的束缚态**。在实验上，我们可以通过**绝热的**将磁场减小，扫过Feshbach共振点来制备弱束缚的分子态。

### 宽共振与窄共振

现在，我们重新考虑初始时的散射能量对散射长度的影响。假设散射能量为 $E$，可以进一步得到此时的散射长度写为：
$$
a_s(E)=a_{bg}\left(1-\dfrac{\mu\Delta}{\mu(B-B_{res})+E}\right)
$$
利用展开式：
$$
a_s(E)=a_s+\dfrac12k^2a_s^2r_{\text{eff}},\quad E=\dfrac{\hbar^2k^2}{2m}
$$
得到：
$$
r_{\text{eff}}=-\dfrac{2\hbar^2\Delta}{\mu ma_{bg}(B-B_{res}-\Delta)^2}\approx-\dfrac{2\hbar^2}{\mu m a_{bg}\Delta}
$$
第二步近似在共振点附近成立。此式指出有效范围 $r_{\text{eff}}$ 取决于 $\gamma$ 。这是第2.1节讨论的单散射通道模型与本节讨论的双通道模型之间的主要区别。在单通道模型中（如第2.1节所述），可以通过微调势能使阈值处存在束缚态，这种共振也被称为**形状共振**。通常对于 $s$ 波形状共振，$r_{\text{eff}}$ 值通常可以忽略不计。但对于双通道模型，根据开放通道与闭合通道之间混合强度的不同，有效范围可在极小到极大范围内进行调节，且 $r_{\text{eff}}$ 的符号取决于 $a_{bg}$ 的符号。也就是说，只有当Feshbach共振中的 $\Delta$ 足够大时，$r_{\text{eff}}$ 值足够小，双通道模型中的Feshbach共振才等同于单通道模型中的形状共振。
为表征有效范围在多体简并费米气体系统中的作用，引入了无量纲量 $k_Fr_{\text{eff}}$：
$$
k_Fr_{\text{eff}}=\dfrac{4E_F}{\mu\Delta(k_Fa_{bg})}
$$
当 $k_Fr_{\text{eff}}\ll 1$ 时，称其为**宽共振**(wide resonance)；而当 $k_Fr_{\text{eff}}\gg 1$ 时，称其为**窄共振**(narrow resonance)。对于窄共振而言，散射长度在 $E_F$ 能量范围内变化显著，因此多体系统无法通过单一与能量无关的散射长度参数来描述。












