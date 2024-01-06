# 证明交比不变性：
交比定义为距离比的比值，在一维空间中的齐次坐标系下，可以使用行列式表示：
$$
\mathrm{Cross}(A,B,C,D)=\frac{
  |AC||AD|
}{|BC||BD|}
$$
式中，
$$
|AC|=\det\begin{bmatrix}
  x_A & x_C  \\
  y_A& y_C  \\
\end{bmatrix}
$$
是前两项的行列式，因此可设：
$$
\begin{aligned}
\mathbf{A}'=s_1\mathbf{HA}\\
\mathbf{B}'=s_2\mathbf{HB}\\
\mathbf{C}'=s_3\mathbf{HC}\\
\mathbf{D}'=s_4\mathbf{HD}
\end{aligned}
$$
代入行列式中，得：
$$
\begin{aligned}
|A'B'|=\det\begin{bmatrix}
  s_1\mathbf{HA}& s_2\mathbf{HB}  
\end{bmatrix}=s_1s_2\det(\mathbf{H})|AB|
\end{aligned}
$$
同理可得：
$$
\begin{aligned}
|A'C'|=s_1s_3\det(\mathbf{H})|AC|\\
|A'D'|=s_1s_4\det(\mathbf{H})|AD|\\
|B'C'|=s_2s_3\det(\mathbf{H})|BC|\\
|B'D'|=s_2s_4\det(\mathbf{H})|BD|\\
\end{aligned}
$$
代入交比定义，即可验证四个比例因子和行列式$\det\mathbf{H}$均被消去，原式得证。

# 证明仿射变换能把圆映射成椭圆但是不能映射成双曲线和抛物线：
根据二次曲线的仿射分类可知，与无穷远直线没有交点的二次曲线是椭圆或者圆，有一个交点的二次曲线是抛物线，有两个交点的二次曲线是双曲线。仿射变换不改变无穷远直线，而交点性质是射影变换都不会改变的，因此经过仿射变换后，曲线与无穷远直线的交点数量不会变化，所以圆不会变成双曲线和抛物线，而可能变成椭圆。
# 证明仿射变换下平行的两条线段长度之比不变，而不平行的则不然
设平行线段$AB$和$CD$，则有：
$$
\begin{aligned}
\mathbf{A-B}=&\lambda(\mathbf{C-D})\\
\frac{|AB|}{|CD|}=&\lambda
\end{aligned}
$$
其中$\lambda$为常数，设仿射变换为$\mathbf{X}'=\mathbf{HX}$，则有：
$$
\mathbf{H}=\begin{bmatrix}
  \mathbf{A}& \mathbf{v}\\
   0&1\\
\end{bmatrix}
$$
当平行线段的端点ABCD不含有无穷远点时，经过仿射变换后，有：
$$
\begin{aligned}
\mathbf{A}'=\begin{bmatrix}
\mathbf{AX}_A+\mathbf{v}z_A\\
z_A
\end{bmatrix}
\end{aligned}
$$
因此两平行线段的长度相应地变化为：
$$
\begin{aligned}
|A'B'|=&\sqrt{(\mathbf{X}_A-\mathbf{X}_B)^T\mathbf{A}^T\mathbf{A}(\mathbf{X}_A-\mathbf{X}_B)}\\
|C'D'|=&\sqrt{(\mathbf{X}_C-\mathbf{X}_D)^T\mathbf{A}^T\mathbf{A}(\mathbf{X}_C-\mathbf{X}_D)}\\
=&\lambda\sqrt{(\mathbf{X}_A-\mathbf{X}_B)^T\mathbf{A}^T\mathbf{A}(\mathbf{X}_A-\mathbf{X}_B)}\\
\end{aligned}
$$
因此两线段长度之比不变。对于不平行的线段，由于公式（第一项）不成立，因此其长度之比不能保持不变。
