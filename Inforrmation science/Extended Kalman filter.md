卡尔曼滤波的一个限制是状态方程和测量方程都必须是线性的，扩展卡尔曼滤波可以解决这一限制。在扩展卡尔曼滤波中，状态方程和测量方程满足如下形式
$$
\begin{aligned}
x_t &= g(u_t, x_{t - 1}) + \epsilon_t
\\
z_t &= h(x_t) + \delta_t
\end{aligned}
$$ 
