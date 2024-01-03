$$
\begin{gathered}
\operatorname{tr}(\mathrm{ABCD})=\operatorname{tr}(\mathrm{DABC})=\operatorname{tr}(\mathrm{CDAB})=\ldots \quad \operatorname{tr}(\mathrm{A}+\mathrm{B})=\operatorname{tr}(\mathrm{A})+\operatorname{tr}(\mathrm{B}) \\
\operatorname{tr}(\mathrm{AB})=\operatorname{tr}\left(\mathrm{A}^{\mathrm{T}} \mathrm{B}^{\mathrm{T}}\right) \\
(\mathrm{AB})^{\mathrm{T}}=\mathrm{B}^{\mathrm{T}} \mathrm{A}^{\mathrm{T}}(\mathrm{A}+\mathrm{B})^{\mathrm{T}}=\mathrm{A}^{\mathrm{T}}+\mathrm{B}^{\mathrm{T}} \\
(\mathrm{ABC})^{\mathrm{T}}=\mathrm{C}^{\mathrm{T}}(\mathrm{AB})^{\mathrm{T}}=\mathrm{C}^{\mathrm{T}} \mathrm{B}^{\mathrm{T}} \mathrm{A}^{\mathrm{T}} \\
\text { 图像 } a \text { 有m 个特征点, 图像 } b \text { 有 } n \text { 个特征点 } \\
\text { 维度: } \mathrm{A}(\mathrm{n}, \mathrm{m}) \quad f_{1}(3, m) \quad f_{2}(3, n) \quad 1(m, 1) \quad R(3,3) \quad t(3,1) \\
\left\|R f_{1}+t 1^{T}-f_{2} A\right\|_{F}^{2} \\
=\left\|t 1^{T}+R f_{1}-f_{2} A\right\|_{F} \\
=\operatorname{tr}\left(t t^{T}\right)+\operatorname{tr}\left(1^{T} f_{1}{ }^{T} R^{T} t\right)-\operatorname{tr}\left(1^{T} A^{T} f_{2}{ }^{T} t\right)+\operatorname{tr}\left(R f_{1} 1 t^{T}\right)+\operatorname{tr}\left(f_{1} f_{1}{ }^{T} R^{T} R\right)-\operatorname{tr}\left(f_{1} A^{T} f_{2}{ }^{T} R\right) \\
-\operatorname{tr}\left(f_{2} A 1 t^{T}\right)-\operatorname{tr}\left(f_{2} A f_{1}{ }^{T} R^{T}\right)+\operatorname{tr}\left(f_{2}{ }^{T} f_{2} A A^{T}\right) \\
\operatorname{tr}\left(R f_{1} 1 t^{T}\right)=\operatorname{tr}\left(R f_{1} 1 t^{T}\right)=\operatorname{tr}\left(\left(R f_{1} 1\right)^{T} t\right)=\operatorname{tr}\left(1^{T} f_{1}{ }^{T} R^{T} t\right) \\
\operatorname{tr}\left(f_{2} A 1 t^{T}\right)=\operatorname{tr}\left(\left(f_{2} A 1\right)^{T} t\right)=\operatorname{tr}\left(1^{T} A^{T} f_{2}{ }^{T} t\right)
\end{gathered}
$$

整理关于 t 的项并去除trace: 
$$
t t^{T}+1^{T} f_{1}{ }^{T} R^{T} t-1^{T} A^{T} f_{2}{ }^{T} t+1^{T} f_{1}{ }^{T} R^{T} t-1^{T} A^{T} f_{2}{ }^{T} t+\ldots
$$
求导: 
$$
2 t+2 R f_{1} 1-2 f_{2} A 1=0
$$

$$
t^{*}=f_{2} A 1-R f_{1} 1
$$

代入原方程: 
$$
\left\|R f_{1}+f_{2} A 11^{T}-R f_{1} 11^{T}-f_{2} A\right\|_{F}^{2}\\
=\left\|R f_{1}\left(I_{m}-11^{T}\right)-f_{2} A\left(I_{m}-11^{T}\right)\right\|_{F}^{2}\\
=\left\|\left(R f_{1}-f_{2} A\right)\left(I_{m}-11^{T}\right)\right\|_{F}^{2}
$$
交替优化

$$
\begin{gathered}
\left\|R f_{1}\left(I_{m}-11^{T}\right)-I_{3} f_{2} A\left(I_{m}-11^{T}\right)\right\|_{F}^{2} \\
=\left\|R a-I_{3} b\right\|_{F}^{2} \\
=\left\|\left[\begin{array}{ll}
I_{3}
\end{array}\right]\left[\begin{array}{c}
a \\
-b
\end{array}\right]\right\|_{F}^{2} \\
=\|T G\|_{F}^{2}=\operatorname{tr}\left(T G G^{T} T^{T}\right)
\end{gathered}
$$