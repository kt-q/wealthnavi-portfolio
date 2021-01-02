# WealthNaviのポートフォリオ最適化について  
- コードの参考URL: https://datacoach.me/investment/long-inv/python-wealthnavi/
- [WealthNaviの資産運用アルゴリズム](https://www.wealthnavi.com/image/WealthNavi_WhitePaper.pdf)
  - 平均分散法によって資産クラスの最適化を行う
  - リスク許容度に応じた最適ポートフォリオは以下の（非線形）最大化問題の解となる資産配分比率(w)を求めることによって求まる

$$
max(\mathbf{w})  \quad  \mathbf{r^T w} - \frac{1}{2 \lambda} \mathbf{w^T \Sigma w} \\
s.t.  \  \mathbf{w^T 1}=1,  \  a \leqq \mathbf{w} \leqq b \\
$$

$$
\begin{aligned}
  & \mathbf{r}: & &各資産クラスの期待リターン  \\
  & \mathbf{\Sigma}: & &分散・共分散行列  \\
  & \mathbf{w}: & &各資産クラスへの配分比率  \\
  & \mathbf{\lambda}: & &リスク許容度（1 - 5）に応じた係数  \\
  & \mathbf{a}: & &各銘柄への配分比率の下限  \\
  & \mathbf{b}: & &各銘柄への配分比率の上限  \\
\end{aligned}
$$

