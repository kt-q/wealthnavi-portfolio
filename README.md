# WealthNaviのポートフォリオ最適化について  
- コードの参考URL: https://datacoach.me/investment/long-inv/python-wealthnavi/
- [WealthNaviの資産運用アルゴリズム](https://www.wealthnavi.com/image/WealthNavi_WhitePaper.pdf)
  - 平均分散法によって資産クラスの最適化を行う
  - リスク許容度に応じた最適ポートフォリオは以下の（非線形）最大化問題の解となる資産配分比率(w)を求めることによって求まる

<img src="https://github.com/kt-q/wealthnavi-portfolio/blob/master/fig/equation_texclip20210102211142.png" width="250" height="auto">

**r**:  各資産クラスの期待リターン <br>
**Σ**:  quad 分散・共分散行列 <br>
**w**:  各資産クラスへの配分比率 <br>
**λ**:  リスク許容度（1 - 5）に応じた係数 <br>
**a**:  各銘柄への配分比率の下限 <br>
**b**:  各銘柄への配分比率の上限 <br>
