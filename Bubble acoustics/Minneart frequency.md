气体形成气泡时，在气泡闭合的瞬间它会发生振动。气泡周围的液体会因为惯性挤压气泡壁使其向内收缩，而气泡内的气体会因为弹性使得气泡向外部扩张。这种振动在简化的条件下可以使用非常简洁的方程描述出来。

![[bubble-resonance.png|239]]

气泡的模型如图假设气泡的瞬时半径为$R(t)$（稳态半径为$R_0$），作用于气泡壁上的瞬时压强为$P(t)$（稳态压强为$P_0$）。那么有
$$
    R(t)=R_0+\xi,\quad P(t)=P_0+p(t)
$$
其中$\xi$和$p$分别代表了半径位移和压强的扰动。那么根据气体绝热过程的拉普拉斯定律有：
$$
    P_0 R_0^{3\gamma}=P(t)R(t)^{3\gamma} \longrightarrow p(\xi)=P_0\left[\left(1+\frac{\xi}{R_0}\right)^{-3\gamma}-1\right]
$$
假设气泡的振动频率远小于气泡半径，即$|\xi|\ll R_0$，那么上式可以被线性化为：
$$
    p(\xi)\simeq-3\gamma P_0\frac{\xi}{R_0}
$$
当气泡的半径从$R_0$变为$R_0+\xi$，其势能做功为：
$$
E_{\mathrm{p}}(\xi)=-\int_{0}^{\xi} 4 \pi\left(R_{0}+\xi^{\prime}\right)^{2} \mathrm{~d} \xi^{\prime} p\left(\xi^{\prime}\right)
$$
使用式\eqref{linearP}中的线性化近似可以得到：
$$
    E_\text{p}(\xi)\simeq\frac{1}{2}K\xi^2,\quad K=12\pi\gamma R_0 P_0
$$
为了得到气泡外液体的动能，假设液体是近似不可压缩的。在极坐标下令$\vec{v}$是液体的运动速度，同时气泡外液体的速度是无源的$\nabla\cdot\vec{v}=0$,那么液体的运动速度有：
$$
\vec{v}(\vec{r}, t)=\dot{\xi}(t) \frac{\left(R_{0}+\xi(t)\right)^{2}}{r^{2}} \vec{e}_{r}
$$
其中$\vec{e}_r$是径向方向的单位向量。令$\rho_w$为外部液体的密度，且不随液体的运动变化，那么有：
$$
E_{\mathrm{k}}(\xi, \dot{\xi})=\frac{1}{2} \rho_{w} \int_{R_{0}+\xi}^{\infty} 4 \pi r^{2} \mathrm{~d} r v^{2}=\frac{1}{2} M(\xi) \dot{\xi}^{2},\quad M(\xi)=4 \pi \rho_{w}\left(R_{0}+\xi\right)^{3}
$$
上式可以被线性化为：
$$
E_{\mathrm{k}}(\dot{\xi}) \simeq \frac{1}{2} M \dot{\xi}^{2},\quad M=M(\xi=0)=4 \pi \rho_{w} R_{0}^{3}
$$
经过以上的假设以及线性化近似，并根据势能 $E_\text{p}$ 和动能 $E_\text{k}$ 相等，可以看到气泡壁的振动模式相当于一个弹簧振子，则其自然频率就可以表示为：
$$
    f_r=\frac{1}{2\pi}\sqrt{\frac{K}{M}}=\frac{1}{2\pi R_0}\sqrt{\frac{3\gamma P_0}{\rho_w}}
$$
以上推导过程最先由Minneart推导[1] ，因此该气泡谐振频率又称为Minneart频率。

[1] M. Minnaert, “XVI. On musical air-bubbles and the sounds of running water,” _The London, Edinburgh, and Dublin Philosophical Magazine and Journal of Science_, vol. 16, no. 104, pp. 235–248, Aug. 1933, doi: [10.1080/14786443309462277](https://doi.org/10.1080/14786443309462277).