---
title: Differential calculus
layout: post
date: 2014-11-30 21:00:00
postTitle: Derivative applications
categories: differential
---

-------

# Equations of normal and tangent lines

--------

## y-intercept of tangent line example

<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">
    曲線\(f(x)=\frac{1}{x}\)のある点\((k \ne 0)\)における接線が
    \(y\)軸を横切るときの値を求めよ
    <br>
    \(x=k\)の点の座標は\( (k,\frac{1}{k}) \)
    <br>
    この点を通る接線の傾きは
    $$f(x)=\frac{1}{x}=x^{-1}$$
    $$f'(x)=-x^{-2}=-\frac{1}{x^2}$$
    \(x=k\)のときの傾きは
    $$f'(k)=-\frac{1}{k^2}$$
    接線(tangent line)を\(y=mx+b\)とすると
    <br>
    傾き\(m=\frac{1}{k^2}\)、　ｙ軸との交点のy座標は\(b\)なので
    $$y=-\frac{1}{k^2}x+b$$
   　点\( (k,\frac{1}{k}) \)を通るので
    $$\frac{1}{k}=-\frac{1}{k^2}k+b$$
    $$\frac{1}{k}=-\frac{1}{k}+b$$
    $$b=\frac{1}{k}+\frac{1}{k}=\frac{2}{k}$$
    したがって点\( (k,\frac{1}{k}) \)を通る接線の式は
    $$y=-\frac{1}{k^2}x+\frac{2}{k}$$

  </div>
</div>

-------------

## Equation of normal line(法線)

幾何において __normal__　とは、与えられたオブジェクトに対して垂直な線やベクトルなどのオブジェクトです。

２次元の場合、曲線上の任意の点における接線に対してその点を通る垂直な直線を法線(noramal line)といいます。

<div class="row">
  <div class="col-sm-6">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-6">
  曲線\(f(x)=\frac{e^x}{x^2}\)で\(x=1\)のときの法線の式を求める
  <br>
  \(x=1\)のときの接線の傾きを求めます  
  $$f(x)=\frac{e^x}{x^2}=e^xx^{-2} \quad
  f(1)=\frac{e^1}{1^2}=e$$
  \(f(x)\)を微分します
  $$f'(x)=e^xx^{-2}+e^x(-2x^{-3})$$
  $$f'(1)=e-2e=-e \quad 接線の傾き$$
  法線の傾きは\(-\frac{1}{m}\)なので\(\frac{1}{e}\)
  <br>
  \(y=-\frac{1}{m}x+b\)を法線の式とすると
  $$e=\frac{1}{e}+b \to b=e-\frac{1}{e}$$
  $$y = \frac{1}{e}x+e-\frac{1}{e}$$

  </div>
</div>

---------------

# Motion along a line

導関数はその瞬間の変化の割合を計算することができます。
時間に対し位置変化の割合が速度(velocity)で、
時間に対し速度変化の割合が加速度(acceleration)です。
この考え方を使って、時間の関数として表される位置にある１次元の粒の動きを分析してみましょう。

-----------

## Total distance traveled by a particle

<div class="row">
  <div class="col-sm-6">
    <div class="panel">
    数直線上をうごく粒子の位置は下記の式で表されるとします
    $$s(t)=\frac{2}{3}t^3-6t^2+10t \quad (t \ge 0)$$
    tは秒を表します
    <br>
    粒子は最初の６秒間に左右に動きます。\(0 \le t \le 6\)の間に粒子が移動する距離の合計はどれだけですか？
    </div>
    右方向に動くときを　＋　、左方向に動くときを　―　で表します。
    <br>
    \(s(t)\)を微分して、速度の変化を表す式を求めます
    $$s'(t)=2t^2-12t+10$$
    \(s'(t)=0\)のとき速度は0で、その時のtを求めます
    $$2t^2-12t+10=0$$
    $$t^2-6t+5=0$$
    $$(t-1)(t-5)=0$$
    したがって\(t=1\)または\(t=5\)のときに速度は0となります。
    <br>
    \(0 \le t \le 1\)で粒子は右方向へ移動し、
    \(1 \le t \le 5\)で粒子は左方向へ移動し、
    \(5 \le t \le 6\)で粒子は右方向へ移動します
    <br>
    １秒後の位置は\(4\frac{2}{3}\)なので移動距離は\(4\frac{2}{3}\)<br>
    5秒後の位置は\(-16\frac{2}{3}\)なので、
    まず\(4\frac{2}{3}\)で最初の位置へ戻りさらに\(16\frac{2}{3}\)移動します<br>
    ６秒後の位置は\(-12\)なので、移動距離は\(4\frac{2}{3}\)<br>
    距離の合計は
    $$4\frac{2}{3}+4\frac{2}{3}+16\frac{2}{3}+4\frac{2}{3}
    =30\frac{2}{3}$$
  </div>
  <div class="col-sm-6">
    <div id="svg03"></div>
    <table class="table">
      <thead>
        <th>\(t\)</th>
        <th>\(s(t)\)</th>
      </thead>
      <tbody>
        <tr>
          <td>0</td>
          <td>0</td>
        </tr>
        <tr>
          <td>1</td>
          <td>\(4\frac{2}{3}\)</td>
        </tr>
        <tr>
          <td>5</td>
          <td>\(-16\frac{2}{3}\)</td>
        </tr>
        <tr>
          <td>6</td>
          <td>-12</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

----------

## When is a particle speeding up?
<div class="row">
  <div class="col-sm-6">
    数直線上を粒子が左右に行ったり来たりします
    <div id="svg04"></div>
    粒子の位置を時間で表す関数を
    \(s(t)=t^3-6t^2+9t、ｔ \ge 0\)とします<br>
    "スピードアップ"とはどういうことでしょうか<br>
    右方向へスピードアップするとは、速度が正\(v(t) \gt 0\)であり、加速度が正\(a(t) \gt 0\)ということです<br>
    左方向へスピードアップするとは、速度が負\(v(t) \lt 0\)であり、加速度が負\(a(t) \lt 0\)ということです<br>
    速度が正（右向き）のとき、加速度が負（左向き）の場合、スピードは遅くなります、
    速度が負（左向き）のとき、加速度が正（右向き）の場合も、スピードは遅くなります。<br>

    時間に対する位置の変化は位置を表す関数\(s(t)\)の導関数で、それは速度を表しますす
    $$s'(t)=\frac{ds}{dt}=v(t)$$
    $$v(t)=3t^2-12t+9$$
    このグラフを描きます、その時 \(v\)軸との交点は\(v(0)=9\)です<br>
    \(t\)軸との交点は
    $$3t^2-12t+9=0$$
    両辺を３で割ります
    $$t^2-4t+3=0 \to (t-1)(t-3)=0$$
    $$t=1 \quad or \quad t=3$$
    次に、時間に対する速度の変化は\(v(t)\)の導関数で、加速度を表します
    $$s"(t)=v'(t)=a(t)=6t-12$$
    \(v(t)\)の点\((t,v(t))\)における接線の傾きです<br>
    スピードアップの条件は
    $$v(t) \gt 0 \quad and \quad a(t) \gt 0 \quad または \quad
    v(t) \lt 0 \quad and \quad a(t) \lt 0$$
    よって
    $$1 \lt t \lt 2 \quad or \quad t \gt 3$$
  </div>
  <div class="col-sm-6">
    <div id="svg05"></div>
  </div>
</div>

--------------

# Critical points and graphing with calculus

---------------

## Minima, maxima and critical points

<div class="row">
  <div class="col-sm-6">
  関数\(f(x)\)の曲線において<br>
  最大値は\((x_{0},f(x_{0}))\)の点でグローバル最大値（global maximum）といいます。
  この点における接線の傾きは0、つまり\(f'(x_{0})=0\)です<br>
  最小値は、マイナスの無限大と考えられるためグローバル最小値は、存在しません<br>
  ローカル最小値は \((x_{1},f(x_{1}))\)の点です。この点における接線の傾きは0、つまり\(f'(x_{1})=0\)です<br>
  ローカル最大値は \((x_{2},f(x_{2}))\)の点です。この点では接線は定義できません、つまり\(f'(x_{2})=undefined\)です<br>
  両端（end points）ではい、\(x=a\)の点で、最大値や最小値がある、<br>
  つまり、\(f'(a)=0\)または\(f'(a)\)は未定義となる点をcritical pointと呼びます
  </div>
  <div class="col-sm-6">
    <div id="svg06"></div>
  </div>
</div>

-----------------

## Finding critical numbers

\\(f(x)=xe^{-2x^2}\\)のクリティカル数を求めます

\\(c\\)を\\(f\\)のクリティカル数とします

\\(f'(c)=0\\) または \\(f'(c)\\)未定義のとき、\\(c\\)はクリティカル数です

\\(f(x)\\)の導関数を求めます

$$f'(x)=\frac{d}{dx}[x]e^{-2x^2}+\frac{d}{dx}[e^{-2x^2}]x$$
$$\quad = e^{-2x^2}+e^{-2x^2}(-4x)x$$
$$\quad =e^{-2x^2}(1-4x^2)$$
$$1-4x^2=0$$
$$1=4x^2$$
$$x=\pm\frac{1}{2}$$
したがって、クリティカル数は\\(\frac{1}{2},-\frac{1}{2}\\)です

-----------------

## Testing critical points for local extrema(極値)

<div class="row">
  <div class="col-sm-6">
    クリティカル・ポイントが、最大値か最小値かを調べるには<br>
    点の前後で傾きの符号がどう変わったかを調べます<br>
    \(x=x_{0}\)では、傾きは正から負へと変わります<br>
    \(x=x_{2}\)でも、傾きは正から負へと変わります<br>
    傾きの符号が正から負に代わる点は最大値です<br>
    \(x=x_{1}\)では、傾きは負から正へと変わります<br>
    傾きの符号が負から正に代わる点は最小値です<br>
    \(x=x_{3}\)では、傾きは負から負です<br>
    この点はクリティカル・ポイントではありません
  </div>
  <div class="col-sm-6">
    <div id="svg07"></div>
  </div>
</div>


-----------------

## Identifying minima and maxima for \\(x^3 - 12x + 2\\)

<div class="row">
  <div class="col-sm-6">
   \(f(x)=x^3 - 12x + 2\) にクリティカル・ポイントがあるか調べます<br>
   \(f(x)\)の導関数を求めます
   $$f'(x)=3x^2-12$$
   $$3x^2-12=0$$
   $$3x^2=12$$
   $$x^2=4$$
   $$x=\pm2$$
   $$f'(2)=0 \quad f'(-2)=0$$
   \(f(x)\)にはクリティカル・ポイントがあります
   $$$$
   \(x=-2\)で、傾きの符号が正から負へ変わるので、最大値です<br>
   \(x=2\)で、傾きの符号が負から正へ変わるので、最小値です<br>
  </div>
  <div class="col-sm-6">
    <div id="svg08"></div>
  </div>
</div>

--------------

# Absolute and relative maxima and minima

--------------

## Extreme value theorem　(極値定理)

<div class="row">
  <div class="col-sm-6">
  関数\(f(x)\)が閉じた区間(\(a,b\)を含む)\([a,b]\)において連続であるならば<br>
  \(f(x)\)には、最大値と最小値が存在する<br>
  \(x=c\)のとき最小値、\(x=d\)のとき最大値とすると
  $$\exists c,d \in [a,b]$$
  $$f(c) \le f(x) \le f(d)$$
  である
  </div>
  <div class="col-sm-6">
    <div id="svg09"></div>
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
  関数\(f(x)\)が不連続の場合、<br>
  \(x=c\)に限りなく近づいて行くと\(f(c)\)に限りなく近づきますがそこには値がありません<br>
  \(x=d\)に限りなく近づいて行くと\(f(d)\)に限りなく近づきますがそこには値がありません<br>
  したがって、不連続の関数では、最大値と最小値が存在するとは限りません。
  </div>
  <div class="col-sm-6">
    <div id="svg091"></div>
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
  開いた（\(a,b\)を含まない）区間\((a,b)\)では、<br>
  \(x=a\)に限りなく近づいて行くと\(f(a)\)に限りなく近づきますがそこには値がありません<br>
  \(x=b\)に限りなく近づいて行くと\(f(b)\)に限りなく近づきますがそこには値がありません<br>
  したがって、開いた区間では関数に、最大値と最小値が存在するとは限りません。
  </div>
  <div class="col-sm-6">
    <div id="svg092"></div>
  </div>
</div>

--------------

## Relative minima and maxima

<div class="row">
  <div class="col-sm-6">
    <div id="svg10"></div>
  </div>
  <div class="col-sm-6">
  関数\(f(x)\)は閉じた区間\([a,b]\)において、\(x=a\)のとき最大であり<br>
  \(x=b\)のとき最少である<br>
  <br>
  \(x=c\)のとはどうでしょうか<br>
  最小値ではないが、\(x=c\)では、その近くの点よりは小さい<br>
  これをrelative minimum または local minimum と呼ぶ
  $$f(c)\le f(x) \quad \forall x \in (c-h,c+h), h \gt 0$$
  \(x=d\)のとはどうでしょうか<br>
  最大値ではないが、\(x=d\)では、その近くの点よりは大きい<br>
  これをrelative maximum または local maximum と呼ぶ
  $$f(d)\ge f(x) \quad \forall x \in (c-h,c+h), h \gt 0$$
  </div>
</div>

--------------

# Concavity and inflection points

---------------

## Concavity, concave upwards and concave downwards intervals

<div class="row">
  <div class="col-sm-6">
    <div id="svg11"></div>
  </div>
  <div class="col-sm-6">
    白線：関数\(f(x)\)<br>
    ピンク：\(f(x)\)の１次導関数\(f'(x)\)<br>
    緑線：\(f(x)\)の２次導関数\(f''(x)\),\(f'(x)\)の１次導関数<br><br>

    関数\(f(x)\)は\(x \ge 0 \)の表示範囲で、最大値と最小値があります<br>
    それらの点はクリティカル・ポイントです<br><br>
    最大値の近くでは\(x\)の小さい方から最大値に近づいていくと、
    その接線の傾きは正の値が徐々に小さくなり、最大値で0となり、それを過ぎると負の値となりさらに小さくなっていきます。<br><br>
    最少値の近くでは\(x\)の小さい方から最少値に近づいていくと、
    その接線の傾きは負の値が徐々に大きくなり、最少値で0となり、それを過ぎると正の値となりさらに大きくなっていきます。<br><br>
    最大値の近くでは、関数\(f(x)\)の描く曲線は下を向いた凹み(concave downward)となります<br>
    最少値の近くでは、関数\(f(x)\)の描く曲線は上を向いた凹み(concave upward)となります<br><br>
    
    クリティカル・ポイントが最大値か最小値かは、凹みの向きを調べればわかります<br>
    
    concave downwardの条件は<br>
    関数\(f(x)\)の接線の傾きが減少していて\(f''(x) \lt 0\)<br>
    この時クリティカル・ポイントは最大値です。<br>
    
    concave upwardの条件は<br>
    関数\(f(x)\)の接線の傾きが増加していて\(f''(x) \gt 0\)<br>
    この時クリティカル・ポイントは最少値です。
  </div>
</div>

--------------

## An inflection point (反曲点)

<div class="row">
  <div class="col-sm-6">
    <div id="svg12"></div>
  </div>
  <div class="col-sm-6">
    関数\(f(x)\)の曲線が、下向きの凹みから上向きの凹み点はどこでしょうか。<br>
    その点は、関数\(f(x)\)の１次導関数\(f'(x)\)の極値を示す点であり<br>
    関数\(f(x)\)の２次導関数\(f''(x)\)の符号が変わる点です。
  </div>
</div>


--------------

# Optimization with calculus

--------------

## Minimizing sum of squares

<div class="panel">
２つの数\(x\)と\(y\)があり、この積が\(xy=-16\)のとき、それぞれの２乗の和\(x^2+y^2\)の最少値を求めよ。
</div>

\\(S=x^2+y^2\\)において\\(S\\)の値を最少にする

\\(xy=-16　\to y=-\frac{16}{x}\\)

\\(S\\)を\\(x\\)の関数として表すと

$$S(x)=x^2+(-\frac{16}{x})^2=x^2+256x^{-2}$$

１次導関数を求める
$$S'(x)=2x-512x^{-3}$$

critical pointsを求める

$$2x-512x^{-3}=0$$
$$2x=512x^{-3}$$
$$2x \cdot x^3 = 512x^{-3} \cdot x^3$$
$$2x^4=512$$
$$x^4=256$$
$$x^2=16$$
$$x=\pm 4$$

\\(x=-4,y=4\\) or \\(x=4,y=-4\\)

２次導関数を求める
$$S''(x)=2+3 \cdot 512x^{-4}$$
\\(2+3 \cdot 512x^{-4}\\)の値はすべての\\(x\\)で正なので

関数\\(S(x)\\)の描くグラフは上向きの凹　\\(\cup\\)となる

$$S=16 + 16 = 32$$

--------------

##　Optimizing box volume

<div class="row">
  <div class="col-sm-6">
    <div id="svg131"></div>
    縦横\(20cm \times 30cm\) の長方形の厚紙の４隅を１辺\(xcm\)の正方形で切り取ります<br>
  </div>
  <div class="col-sm-6">
    <div id="svg132"></div>
    左図の用紙を折り曲げて容器を作ります
  </div>
</div>
<div class="panel">
この時、容器の容量が最大となる\(x\)と容積を求めよ
</div>

容積を表す関数は

\\(V(x)=x(20-2x)(30-2x)\\)　と表せます

\\(x\\)は、
$$x \ge 0, \quad 20-2x \ge 0 \to 10 \ge x$$
なので

\\(0 \le x \le 10\\) です 

\\(V(0)=0 \quad V(10)=0\\)
となります

\\(V(x)\\)を展開すると

$$V(x)=4x^3-100x^2+600x$$

１次導関数は
$$V'(x)=12x^2-200x+600$$
\\(12x^2-200x+600=0\\) とし

解の公式を使ってクリティカル・ポイントを求めます

$$x=\frac{200 \pm \sqrt{40000-4 \cdot 12 \cdot 600}}{24}$$
$$x \approx 12.74 \quad x \approx 3.92$$
\\(x le 10\\) なので \\(x \approx 3.92\\)

２次導関数を求めます

$$V''(x)=24x-200$$
\\(V''(3.92) \lt 0 \to 下向きに凹　\cap \\) となりこの時の容積が最大になります

$$V(3.92)=1056.3cm^3$$

--------------

## Optimizing profit at a shoe factory

<div class="panel">
  靴製造工場で、ある靴を生産するときの利益を最大にする生産数を求める<br>
  数量：\(x\) 単位は千<br>
  収入：\(r(x)=10x\) １足あたり$10の収入<br>
  費用：\(c(x)=x^3-6x^2+15x\)<br>
  利益：\(p(x)=r(x)-c(x)=10x-x^3+6x^2-15x=-x^3+6x^2-5x\)<br>
  \(p(x)\)が最大となる生産数\(x\)を求める
</div>

クリティカル・ポイントを求めるため１次導関数を求める
$$p'(x)=-3x^2+12x-5$$
$$-3x^2+12x-5=0 \to 3x^2-12x+5=0$$
$$x=\frac{12 \pm \sqrt{144-4 \cdot 3 \cdot 5}}{6}$$
$$x=\frac{12 \pm \sqrt{84}}{6}$$
$$x=\frac{12 + \sqrt{84}}{6} \approx 3.528$$
$$x=\frac{12 - \sqrt{84}}{6} \approx 0.4725$$

２次導関数を求める
$$p''(x)=-6x + 12$$
$$p''(3.528) \lt 0 \to \cap \quad maximum$$
$$p''(0.4725) \gt 0 \to \cup \quad minimum$$
したがって
$$x=3.528$$
$$p(3.528)=13.128 \to $13,128$$


--------------

##　Minimizing the cost of a storage container

<div class="panel">
上部の開いた長方形の容器に、材料を保管するのに\(10m^3\)必要である<br>
容器の底面は、縦の長さは横の２倍である<br>
保管コストは底面に対して\($10/m^2\)、側面に対しては\($6/m^2\)とすると<br>
最も安い容器のコストを求めなさい
</div>

容量:\\(V=10m^3\\)

容器の容量は、底面の横\\((x)\\)、底面の縦\\((2x)\\)、高さ((h)\\)とすると
$$10=x \cdot 2x \cdot h　= 2x^2h \to h= \frac{5}{x^2}$$

底面のコスト\\(10\cdot x \cdot 2x\\)

４側面のコスト\\(2 \cdot 6 \cdot x \cdot h + 2 \cdot 6 \cdot 2x \cdot h\\)

コスト=底面のコスト+４側面のコスト
$$cost=20x^2+12xh+24xh=20x^2+36xh$$
コストを\\(x\\)の関数として表すと
$$c(x)=20x^2+36x\frac{5}{x^2}=20x^2+180x^{-1}$$

クリティカル・ポイントを求めるため１次導関数を求める
$$c'(x)=40x-180x^{-2}$$
$$40x-180x^{-2}=0$$
$$40x=\frac{180}{x-2}$$
$$x^3=\frac{180}{40}=\frac{9}{2}$$
$$x=(\frac{9}{2})^{\frac{1}{3}} \approx 1.65$$

２次導関数を求める
$$c''(x)=360x^{-3}+40$$
$$c''(1.65) \gt 0 \to \cup \quad minimum$$

費用は\\(c(1.65) \approx $163.54\\)

容器は横\\(1.65m\\)、縦\\(3.3m\\)、高さ\\(1.84m\\)

--------

## Expression for combined area of triangle and square

<div class="panel">
長さ\(100m\)のワイヤがあります、このワイヤを２つに切り、片方で正三角形をつくり、
残りで正方形を作ります<br>
この時、２つの面積の和が最少となる正三角形のワイヤの長さは<br>
正三角形に使用するワイヤの長さを\(x\)とします
</div>

正三角形の面積：\\(\frac{1}{2} \cdot \frac{x}{3} \cdot \frac{xsqrt{3}}{6}\\)

正方形の面積：\\( (\frac{(100-x)}{4})^2 \\)

面積の和：\\(A(x)=\frac{\sqrt{3}}{36}x^2 + \frac{(100-x)^2}{16}\\)

１次導関数
$$A'(x)=\frac{\sqrt{3}}{18}x + \frac{2(100-x)(-1)}{16}
=\frac{\sqrt{3}}{18}x+\frac{1}{8}(x-100)
=\frac{\sqrt{3}}{18}x+\frac{1}{8}x-12.5$$

$$\frac{\sqrt{3}}{18}x+\frac{1}{8}x-12.5=0$$
$$x=\frac{12.5}{\frac{\sqrt{3}}{18}+\frac{1}{8}} \approx 56.5m$$

２次導関数
$$A''(x)=\frac{\sqrt{3}}{18}+\frac{1}{8} \gt 0 \to \cup \quad minimum$$

$$正三角形のワイヤの長さ56.5m$$

--------

# Applying differentiation in different fields

--------

## Derivative and marginal cost(限界費用)

<div class="row">
  <div class="col-sm-6">
    <div id="svg14"></div>
  </div>
  <div class="col-sm-6">
  生産数\(q\)に対して、その生産コストを表す関数\(c(q)\)を考えます<br>
  関数\(c(q)\)の導関数は何を表しているのでしょうか？<br>
  関数\(c(q)\)の曲線における接線の傾きです<br>
  接線の傾きは\(\frac{\delta c}{\delta q}\)、生産数が１単位変化したときの、コストの変化を表します。これを限界費用といいます。<br>
  </div>
</div>

-------

# Related rates

-------

## Rates of change between radius and area of circle

<div class="panel">
池に石を落すと、落ちた所を中心に波紋が円形に広がっていゆきます<br>
ある時点で円の半径は\(3cm\)で、波紋は１秒間に\(1cm\)広がるとします<br>
この時の円の面積の変化はどのようになるか求めなさい
</div>
半径を\\(r\\)、円の面積を\\(A\\)とすると

\\(r=3cm \quad \\) \\(A=\pi r^2\\)
 半径の変化\\(\frac{d r}{d t}=1\frac{cm}{sec} \\)

時間に対する円の面積の変化を求めます\\(\frac{d A}{d t}=?\\)

$$\frac{d}{d t}[A]=\frac{d}{d t}[\pi r^2]$$
$$\frac{d A}{d t}=\pi \frac{d}{d t}[r^2]$$
chain rule 
$$\qquad =\pi \frac{d}{d r}[r^2]\frac{d r}{d t}$$
$$\qquad =\pi \cdot 2r\frac{d r}{d t}$$
$$\qquad =\pi  \cdot 2 \cdot 3 \cdot 1 = 6 \pi \frac{cm^2}{sec}$$

-------------

## Rate of change of baloon height

<div class="panel">
気球が垂直に上昇しています。この気球を真下の地面から\(500m\)離れた地点から見ると、
角度\(\frqc{\pi}{4}rad\)の方向に見えます。気球は１分間に\(0.2rad\)で上昇しています、この時の気球の高さの変化率を求めなさい。
</div>
角度を
$$ \theta = \frac{\pi}{4}$$
時間に対する角度の変化率を
$$\frac{d \theta}{d t}=0.2\frac{rad}{min}$$
高さと角度の関係を
$$ \tan \theta = \frac{h}{500} $$
求めるのは時間に対する高さの変化
$$\frac{d h}{d t}= ?$$
時間に対する高さの変化は
$$ \frac{d}{d t}[\tan \theta] 
  = \frac{d}{d t}[\frac{h}{500}] $$
$$\frac{(d \tan \theta)}{d \theta}\frac{d\theta}{dt} 
= \frac{1}{500}\frac{d}{d h}[h]\frac{d h}{d t}$$
$$\sec^2\theta\frac{d\theta}{dt} = \frac{1}{500}\frac{dh}{dt}$$  

$$\cos(\frac{\pi}{4})=\frac{\sqrt{2}}{2}
\quad \cos^2(\frac{\pi}{4})=\frac{2}{4}=\frac{1}{2}
\quad \sec^2(\frac{\pi}{4})=2$$
$$\frac{dh}{dt}=500 \cdot 2 \cdot 0.2 = 200 \frac{m}{min}$$   

------------

## Related rates of water pouring into cone

<div class="panel">
円錐形の容器があります。容器の口の直径は\(4cm\)、高さ\(4cm\)です。<br>
現在高さ\(2cm\)の位置まで水が入っています、水は１秒間に\(1cm^3\)増えていきます<br>
この時の高さの変化を求めなさい
</div>
円錐の体積は、高さを\\(h\\)とすると
$$V=\frac{1}{3}(底面積)h$$
容器の高さと底面の直径は同じなので、水の入った部分の高さと底面の直径は同じになる
$$V=\frac{1}{3}\pi(\frac{h}{2})^{2}h
=\frac{\pi}{12}h^3$$
体積の変化率は
$$\frac{dV}{dt}=1cm^3/sec$$
求めるのは時間に対する高さの変化
$$\frac{dh}{dt}=?$$

$$\frac{dV}{dt}=\frac{d}{dt}[\frac{\pi}{12}h^3]
=\frac{\pi}{12}\frac{d}{dt}[h^3]
=\frac{\pi}{12}\frac{d}{dh}[h^3]\frac{dh}{dt}
=\frac{\pi}{12}\cdot 3h^2 \cdot \frac{dh}{dt}$$
$$1 = \frac{\pi}{12} \cdot 3 \cdot 2^2 \cdot \frac{dh}{dt}$$
$$\frac{dh}{dt}= \frac{1}{\pi}\frac{cm}{sec}$$

--------------

## Rate of change of distance between approaching cars

<div class="panel">
１台の車が交差点Aに向かって南から北上しています。交差点までの距離は\(0.8km\)、時速\(60km\)で進んでいます。もう１台は、東から交差点までの距離\(0.6km\)を時速\(30km\)で向かっています<br>
時間に対する２台の車の距離の変化を求めよ
</div>
交差点までの距離
$$北上している車：y=0.8km \quad 西に向かう車:x=0.6km$$
速度は交差点に向かっているので距離が短くなっているのでマイナスの値となり
$$北上している車：\frac{dy}{dt}=-60km/h \quad 
西に向かう車:\frac{dx}{dt}-30km/h$$
２台の距離をsとっすると
$$s^2=x^2+y^2$$
$$s^2=0.6^2 + 0.8^2 = 1$$
$$s=1$$
時間に対する２台の車の距離の変化は
$$\frac{ds}{dt}=?$$
$$\frac{d}{dt}[s^2]=\frac{d}{dt}{x^2+y^2}$$
$$\frac{d}{ds}[s^2]\frac{ds}{dt}
=\frac{d}{dx}[x^2]\frac{dx}{dt}+\frac{d}{dy}[y^2]\frac{dy}{dt}$$
$$2s\frac{ds}{dt}=2x\frac{dx}{dt}+2y\frac{dy}{dt}$$
$$2\frac{ds}{dt}=2 \cdot 0.6 \cdot -30 + 2 \cdot 0.8 \cdot -60$$
$$2\frac{ds}{dt}= -132$$
$$\frac{ds}{dt}= -66\frac{km}{h}$$

------------

# Mean value theorem

-------------

## Mean value theorem

<div class="row">
  <div class="col-sm-6">
    <div id="svg15"></div>
  </div>
  <div class="col-sm-6">
  関数\(f(x)\)は、閉区間\([a,b]\)で連続であり、
  開区間\((a,b)\)で微分可能であるとすると<br>
  点\((a,f(a))\)と点\((b,f(b))\)の平均変化率は
  $$\frac{\Delta y}{\Delta x}=\frac{f(b)-f(a)}{b-a}$$
  であり、これはピンクの割線の傾きである。<br>
  これと同じ傾きを持つ接線が開区間\((a,b)\)の間にある点\((c,f(c))\)に存在する。
  $$\frac{\Delta y}{\Delta x}=\frac{f(b)-f(a)}{b-a}=f'(c)$$
  </div>
</div>

--------------

## Finding where the derivative is equal to the average change

<div class="row">
  <div class="col-sm-6">
  $$f(x)=x^2 -6x+8　\quad [2,5]$$
  \(c \in(2,5)\)のとき、
  $$f'(c)=\frac{f(5)-f(2)}{5-2}$$
  となる\(c\)を見つける
  $$f(5)=25-30+8=3$$
  $$f(2)=4-4=0$$
  $$f'(c)=\frac{3}{3}=1$$
  $$f'(x)=2x-6=1 \to x=\frac{7}{2}$$
  </div>
  <div class="col-sm-6">
    <div id="svg16"></div>
  </div>
</div>

--------------

##　Maximizing function at value

<div class="panel">
関数\(f\)はすべての\(x\)で微分可能である。<br>
\(f(-2)=3\)で\(f'(x) \le 7\)であるとき<br>
\(f(10)\)がとりうる最大値は？
</div>

$$\frac{\Delta y}{\Delta x}=\frac{f(10)-3}{10-(-2)} \le 7$$
$$\frac{f(10)-3}{12} \le 7$$
$$f(10)-3 \le 84$$
$$f(10) \le 87$$
最大値は \\(87\\)


--------------

# L'Hôpital's rule

--------------

## Introduction to l'Hôpital's rule

導関数を用いて極限を導き出す方法

<div class="panel">
$$\lim_{x \to c}f(x)=0 \quad and \quad \lim_{x \to c}g(x)=0$$
$$\lim_{x \to c}\frac{f(x)}{g(x)}=\frac{0}{0}　\dots 不定形$$ 
$$and \quad \lim_{x \to c}\frac{f'(x)}{g'(x)}=L$$
$$\lim_{x \to c}\frac{f'(x)}{g'(x)} \quad に値が存在し、Lであるならば$$
$$\lim_{x \to c}\frac{f(x)}{g(x)}=L$$  
</div>

<div class="panel">
$$\lim_{x \to c}f(x)=\pm \infty 
\quad and \quad \lim_{x \to c}g(x)=\pm \infty$$
$$\lim_{x \to c}\frac{f(x)}{g(x)}=\frac{\pm \infty}{\pm \infty}　\dots 不定形$$ 
$$and \quad \lim_{x \to c}\frac{f'(x)}{g'(x)}=L$$
$$\lim_{x \to c}\frac{f'(x)}{g'(x)} \quad に値が存在し、Lであるならば$$
$$\lim_{x \to c}\frac{f(x)}{g(x)}=L$$  
</div>

例

$$\lim_{x \to 0}\frac{\sin x}{x}=\frac{0}{0} \dots 不定形$$
$$f(x)=\sin x \quad g(x)=x$$
$$f'(x)=\cos x \quad g(x)=1$$
$$\lim_{x \to 0}\frac{f'(x)}{g'(x)}
=\lim_{x \to 0}\frac{\cos x}{1}=\frac{1}{1}=1$$
したがって極限は
$$\lim_{x \to 0}\frac{\sin x}{x}=1$$

---------------
例１

$$\lim_{x \to 0}\frac{2\sin x - \sin 2x}{x-\sin x} = \frac{0}{0}$$
不定形となるので、ロピタルの定理を使います、
$$\lim_{x \to 0}\frac{2\cos x - 2\cos 2x}{1-\cos x}
=\frax{2-2}{1-1}=\frac{0}{0}$$
$$\lim_{x \to 0}\frac{-2\sin x + 4\sin 2x}{\sin x}=\frac{0}{0}$$
$$\lim_{x \to 0}\frac{-2\cos x + 8\cos 2x}{cos x}
=\frac{6}{1}=6$$
したがって
$$\lim_{x \to 0}\frac{2\sin x - \sin 2x}{x-\sin x} = 6$$

--------------
例２

$$\lim_{x \to \infty}\frac{4x^2-5x}{1-3x^2}=\frac{\infty}{-\infty}$$
$$\lim_{x \to \infty}\frac{8x-5}{-6x}=\frac{\infty}{-\infty}$$
$$\lim_{x \to \infty}\frac{8}{-6}=-\frac{4}{3}$$
$$\lim_{x \to \infty}\frac{4x^2-5x}{1-3x^2}=-\frac{4}{3}$$
次のように考えることもできます
$$\lim_{x \to \infty}\frac{4x^2-5x}{1-3x^2}
=\lim_{x \to \infty}\frac{x^2(4-\frac{5}{x})}{x^2(\frac{1}{x^2}-3)}
=\lim_{x \to \infty}\frac{4-\frac{5}{x}}{\frac{1}{x^2}-3}
=\lim_{x \to \infty}\frac{4-0}{0-3}=-\frac{4}{3}$$

--------------
例３

$$\lim_{x \to 1}(\frac{x}{x-1}-\frac{1}{\ln x})
=\frac{1}{0}-\frac{1}{0}$$
式を変形します
$$\lim_{x \to 1}(\frac{x\ln x-(x-1)}{(x-1)\ln x})=\frac{0}{0}$$
$$\lim_{x \to 1}\frac{\ln x + x\frac{1}{x} - 1}{\ln x + \frac{1}{x}(x-1)}=\lim_{x \to 1}\frac{\ln x}{\ln x + \frac{x-1}{x}}=\frac{0}{0}$$
$$\lim_{x \to 1}
\frac{\frac{1}{x}}
{\frac{1}{x}-x^{-2}(x-1)+\frac{1}{x}}=\frac{1}{1+1}=\frac{1}{2}$$

--------------

## L'Hopital's Rule to solve for variable

--------------

##

--------------

## Proof of special case of l'Hôpital's rule

<div class="panel">
$$f(a)=0 \quad f'(a) は存在する$$
$$g(a)=0 \quad g'(a) は存在する$$
この場合
$$\lim_{x \to a}\frac{f(x)}{g(x)}=\frac{f'(a)}{g'(a)}$$
が成り立つ
</div>
$$f'(a)=\lim_{x \to a} \frac{f(x)-f(a)}{x-a}$$
$$g'(a)=\lim_{x \to a} \frac{g(x)-g(a)}{x-a}$$

$$\frac{f'(a)}{g'(a)}
=\lim_{x \to a}
\frac{\frac{f(x)-f(a)}{x-a}}
     {\frac{g(x)-g(a)}{x-a}}     
=\lim_{x \to a}\frac{f(x)-f(a)}{g(x)-g(a)}
=\lim_{x \to a}\frac{f(x)-0}{g(x)-0}
=\lim_{x \to a}\frac{f(x)}{g(x)}$$

---------------

# Local linearization

---------------

## Local linearization

<div class="row">
  <div class="col-sm-6">
  \(\sqrt{4.36} \approx ?\) のおおよその値を電卓を使わずに求めます<br>
  \(\sqrt{4} = 2 \) は、わかっています、これより少し大きな値だと予想されます<br>
  $$f(x)=\sqrt{x}=x^{\frac{1}{2}}$$
  とします
  \((4,f(4))\)を通る接線を\(L(x)\)としその傾きは
  $$f'(x)=\frac{1}{2}x^{-\frac{1}{2}}$$
  $$f'(4)=\frac{1}{2} \cdot \frac{1}{2}=\frac{1}{4}$$
  この接線上の点\(x\)は
  $$L(x)=f(4)+f'(4)(x-4)$$
  なので
  $$L(4.36)=2 \cdot \frac{1}{4} \cdot 0.36$$
  $$L(4.36)=2.09$$
  したがって
  $$f(4.36) \approx 2.09$$
  電卓で計算すると\(2.088\)です<br>
  この方法を　Local linearization といいます
  </div>
  <div class="col-sm-6">
    <div id="svg17"></div>
    $$白線:f(x) \quad 緑線:接線$$
  </div>
</div>

---------------

##

<div class="row">
  <div class="col-sm-6">
  </div>
  <div class="col-sm-6">
    <div id="svg18"></div>
  </div>
</div>

---------------

##

<div class="row">
  <div class="col-sm-6">
  </div>
  <div class="col-sm-6">
    <div id="svg19"></div>
  </div>
</div>

---------------

##

<div class="row">
  <div class="col-sm-6">
  </div>
  <div class="col-sm-6">
    <div id="svg20"></div>
  </div>
</div>


<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

<script>

/**  */
  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg03 = d3.select("#svg03")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg04 = d3.select("#svg04")
                .append("svg")
                .attr("height",50)
                .attr("width",500)
                .style("background","#000");
  var svg05 = d3.select("#svg05")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg06 = d3.select("#svg06")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg07 = d3.select("#svg07")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg08 = d3.select("#svg08")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg09 = d3.select("#svg09")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg091 = d3.select("#svg091")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg092 = d3.select("#svg092")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg10 = d3.select("#svg10")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg11 = d3.select("#svg11")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg12 = d3.select("#svg12")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg131 = d3.select("#svg131")
                .append("svg")
                .attr("height",300)
                .attr("width",400)
                .style("background","#000");
  var svg132 = d3.select("#svg132")
                .append("svg")
                .attr("height",300)
                .attr("width",400)
                .style("background","#000");
  var svg14 = d3.select("#svg14")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg15 = d3.select("#svg15")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg16 = d3.select("#svg16")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg17 = d3.select("#svg17")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");


  var xScale01 = d3.scale.linear()
                       .domain([-5,5])
                       .range([50,450]);

  var yScale01 = d3.scale.linear()
                       .domain([6,-4])
                       .range([50,450]);

  // 軸
  axesData01 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale01,
    "yScale":yScale01
  };
  drawAxes(svg01,axesData01);

  var pathData011 =[];
  var pathData012 =[];
  for (var i=-0.25;i>-5;i=i-0.01){
    pathData011.push(new Point(i,1/i));
  };
  for (var i=0.16;i<5;i=i+0.01){
    pathData012.push(new Point(i,1/i));
  };
  drawPath(svg01,pathData011,{"stroke":"#fff"},xScale01,yScale01);
  drawPath(svg01,pathData012,{"stroke":"#fff"},xScale01,yScale01);

  // graph
  lineData01 = [
    {"x1":1,"y1":1,"x2":0,"y2":2,"stroke":"#0f0"},
    {"x1":1,"y1":1,"x2":2,"y2":0,"stroke":"#0f0"},
  ];
  drawLine(svg01,lineData01,xScale01,yScale01);

  // circle
  var circleData01 = [
    {"cx":1,"cy":1,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
  ];
  drawCircle(svg01,circleData01,xScale01,yScale01);

  // mathjax
  foData01 = [
    {"x":5.3,
    "y":1.5,
    "text":"$$x$$",
    "fontSize":"20px"},
    {"x":-0.1,
    "y":8.6,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":0.8,
    "y":1,
    "text":"$$k$$",
    "fontSize":"18px"},
    {"x":-0.8,
    "y":2.8,
    "text":"$$\\frac{1}{k}$$",
    "fontSize":"18px"},
    {"x":1,
    "y":5.3,
    "text":"$$f(x)=\\frac{1}{x}$$",
    "fontSize":"18px"}
  ];

  drawMathjax(svg01,foData01,xScale01,yScale01);

  var xScale02 = d3.scale.linear()
                       .domain([-1,5])
                       .range([50,450]);

  var yScale02 = d3.scale.linear()
                       .domain([6,0])
                       .range([50,450]);

  // 軸
  axesData02 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale02,
    "yScale":yScale02
  };
  drawAxes(svg02,axesData02);

  var pathData02 =[];
  for (var i=0.2;i<=5;i=i+0.1){
    pathData02.push(new Point(i,func01(i)));
  };
  drawPath(svg02,pathData02,{"stroke":"#fff"},xScale02,yScale02);

  function func01(p){
    return Math.pow(Math.E,p)/Math.pow(p,2);
  }

  // Lines
  lineData02 = [
    {"x1":0,"y1":2*Math.E,"x2":2,"y2":0,"stroke":"#0f0"},
    {"x1":2,"y1":Math.E+1/Math.E,"x2":-1,"y2":Math.E-2/Math.E,"stroke":"#f0f"},
  ];
  drawLine(svg02,lineData02,xScale02,yScale02);

  // mathjax
  foData02 = [
    {"x":-1.2,
    "y":3.5,
    "text":"$$normal$$",
    "fontSize":"18px"},
    {"x":1,
    "y":5.3,
    "text":"$$f(x)$$",
    "fontSize":"18px"},
    {"x":2,
    "y":2,
    "text":"$$tangent$$",
    "fontSize":"18px"}
  ];

  drawMathjax(svg02,foData02,xScale02,yScale02);



  /*  Total distance traveled by a particle */
  var xScale03 = d3.scale.linear()
                       .domain([0,7])
                       .range([50,450]);

  var yScale03 = d3.scale.linear()
                       .domain([11,-9])
                       .range([50,450]);

  // 軸
  axesData03 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1,2,3,4,5,6],
    "yTickValues":[10],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale03,
    "yScale":yScale03
  };
  drawAxes(svg03,axesData03);

  var pathData03 =[];
  for (var i=0;i<=7;i=i+0.1){
    pathData03.push(new Point(i,func03(i)));
  };
  drawPath(svg03,pathData03,{"stroke":"#fff"},xScale03,yScale03);

  function func03(p){
    return 2*p*p-12*p+10;
  }

  // mathjax
  foData03 = [
    {"x":7,
    "y":1,
    "text":"$$t$$",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":15,
    "text":"$$v$$",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":8,
    "text":"右方向へ",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":-1,
    "text":"左方向へ",
    "fontSize":"18px"},
  ];

  drawMathjax(svg03,foData03,xScale03,yScale03);

  // When is a particle speeding up?
  vecData04 = [
    {"x1":0,"y1":25,"x2":500,"y2":25,"stroke":"#fff"}
  ];
  drawVectorW(svg04,vecData04);

  lineData04 = [
    {"x1":200,"y1":20,"x2":200,"y2":30,"stroke":"#fff"}
  ];
  drawLine(svg04,lineData04);

  circleData04 = [
    {"cx":200,"cy":25,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
  ];
  drawCircle(svg04,circleData04);

  textData04 = [
    {"x":196,"y":45,"text":"0","stroke":"#fff"}
  ];

  drawText(svg04,textData04);

  var xScale05 = d3.scale.linear()
                       .domain([0,5])
                       .range([50,450]);

  var yScale05 = d3.scale.linear()
                       .domain([11,-4])
                       .range([50,450]);

  // 軸
  axesData05 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1,2,3,4],
    "yTickValues":[9],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale05,
    "yScale":yScale05
  };
  drawAxes(svg05,axesData05);

  var pathData05 =[];
  for (var i=0;i<=5;i=i+0.1){
    pathData05.push(new Point(i,func05(i)));
  };
  drawPath(svg05,pathData05,{"stroke":"#fff"},xScale05,yScale05);

  function func05(p){
    return 3*p*p-12*p+9;
  }

  // mathjax
  foData05 = [
    {"x":5,
    "y":1,
    "text":"$$t$$",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":13.5,
    "text":"$$v$$",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":8,
    "text":"右方向へ",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":-1,
    "text":"左方向へ",
    "fontSize":"18px"},
  ];

  drawMathjax(svg05,foData05,xScale05,yScale05);

  // Minima, maxima and critical points
  var xScale06 = d3.scale.linear()
                       .domain([-1,15])
                       .range([50,450]);

  var yScale06 = d3.scale.linear()
                       .domain([7,-1])
                       .range([50,450]);

  // 軸
  axesData06 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale06,
    "yScale":yScale06
  };
  drawAxes(svg06,axesData06,xScale06,yScale06);

  var pathData06 = [];
  for (var i=-2;i<=2;i=i+0.1){
    pathData06.push(new Point(i,-5/8*i*i+7/4*i+4));
  };
  for (var i=1.8;i<=6;i=i+0.1){
    pathData06.push(new Point(i,2*Math.cos(i-1.7)+3.12));
  };

  drawPath(svg06,pathData06,{"stroke":"#fff"},xScale06,yScale06);

  var pathData061 = [
    {"x":6,"y":2.3},
    {"x":7,"y":1},
    {"x":9,"y":0.6},
    {"x":10,"y":0.5},
    {"x":11,"y":0.5},
    {"x":12,"y":0},
    {"x":15,"y":-2},
  ];
  drawPath(svg06,pathData061,{"stroke":"#fff","interPolate":"basis"},xScale06,yScale06);

  lineData06 = [
    {"x1":0,"y1":5.25,"x2":3,"y2":5.25,"stroke":"#ccc"}
   ,{"x1":3.9,"y1":1.1,"x2":5.9,"y2":1.1,"stroke":"#ccc"}
   ,{"x1":1.4,"y1":0,"x2":1.4,"y2":5.25,"stroke":"#ccc","opacity":0.7}
   ,{"x1":4.9,"y1":0,"x2":4.9,"y2":1.1,"stroke":"#ccc","opacity":0.7}
   ,{"x1":6,"y1":0,"x2":6,"y2":2.3,"stroke":"#ccc","opacity":0.7}
   ,{"x1":10.5,"y1":0,"x2":10.5,"y2":0.5,"stroke":"#ccc","opacity":0.7}
  ]
  drawLine(svg06,lineData06,xScale06,yScale06);

  circleData06 = [
    {"cx":1.4,"cy":5.25,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":4.9,"cy":1.1,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":6,"cy":2.3,"r":2,"stroke":"#0f0","fillColor":"#0f0"}
   ,{"cx":10.5,"cy":0.5,"r":2,"stroke":"#0f0","fillColor":"#00f"}
  ];
  drawCircle(svg06,circleData06,xScale06,yScale06);

  // mathjax
  foData06 = [
    {"x":1,
    "y":7,
    "text":"$$global \\quad maximum$$",
    "fontSize":"18px"},
    {"x":5,
    "y":4,
    "text":"$$local \\quad maximum$$",
    "fontSize":"18px"},
    {"x":2,
    "y":2.0,
    "text":"$$local \\quad min$$",
    "fontSize":"18px"},
    {"x":13,
    "y":0.7,
    "text":"$$y=f(x)$$",
    "fontSize":"16px"},
    {"x":1.2,
    "y":1.0,
    "text":"$$x_{0}$$",
    "fontSize":"16px"},
    {"x":5.8,
    "y":1.0,
    "text":"$$x_{2}$$",
    "fontSize":"16px"},
    {"x":4.7,
    "y":1.0,
    "text":"$$x_{1}$$",
    "fontSize":"16px"},
    {"x":10.3,
    "y":1.0,
    "text":"$$x_{3}$$",
    "fontSize":"16px"},
  ];

  drawMathjax(svg06,foData06,xScale06,yScale06);


  drawAxes(svg07,axesData06,xScale06,yScale06);

  drawPath(svg07,pathData06,{"stroke":"#fff"},xScale06,yScale06);

  drawPath(svg07,pathData061,{"stroke":"#fff","interPolate":"basis"},xScale06,yScale06);

  drawLine(svg07,lineData06,xScale06,yScale06);

  drawCircle(svg07,circleData06,xScale06,yScale06);

  drawMathjax(svg07,foData06,xScale06,yScale06);

  // x^3 -12x +2
  var xScale08 = d3.scale.linear()
                       .domain([-3.5,3.5])
                       .range([50,450]);

  var yScale08 = d3.scale.linear()
                       .domain([15,-15])
                       .range([50,450]);

  // 軸
  axesData08 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[-2,2],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale08,
    "yScale":yScale08
  };
  drawAxes(svg08,axesData08,xScale08,yScale08);

  var pathData08 = [];
  for (var i=-3;i<=3;i=i+0.1){
    pathData08.push(new Point(i,3*i*i-12));
  };
  drawPath(svg08,pathData08,{"stroke":"#fff"},xScale08,yScale08);
  var pathData081 = [];
  for (var i=-3;i<=3;i=i+0.1){
    pathData081.push(new Point(i,i*i*i-12*i+2));
  };
  drawPath(svg08,pathData081,{"stroke":"#f0f"},xScale08,yScale08);

  // mathjax
  foData08 = [
    {"x":-1,
    "y":18,
    "text":"$$f(x)$$",
    "fontSize":"18px"},
    {"x":2.5,
    "y":7,
    "text":"$$f'(x)$$",
    "fontSize":"18px"},
  ];

  drawMathjax(svg08,foData08,xScale08,yScale08);

/****
  Absolute and relative maxima and minima
**/
  var xScale09 = d3.scale.linear()
                       .domain([-1,5])
                       .range([50,450]);

  var yScale09 = d3.scale.linear()
                       .domain([5,-1])
                       .range([50,450]);

  // 軸
  axesData09 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale09,
    "yScale":yScale09
  };
  drawAxes(svg09,axesData09);
  drawAxes(svg091,axesData09);
  drawAxes(svg092,axesData09);

  var pathData09 =[];
  function func09(i){
    return 2*Math.cos(2*i)+2.5;
  }
  for (var i=0.5;i<=4;i=i+0.1){
    pathData09.push(new Point(i,func09(i)));
  };
  drawPath(svg09,pathData09,{"stroke":"#fff"},xScale09,yScale09);
  drawPath(svg091,pathData09,{"stroke":"#fff"},xScale09,yScale09);

  // lines
  lineData09 = [
    {"x1":0.5,"y1":0,"x2":0.5,"y2":func09(0.5),"stroke":"#f0f","opacity":0.6},
    {"x1":3.9,"y1":0,"x2":3.9,"y2":func09(3.9),"stroke":"#f0f","opacity":0.6},
    {"x1":1.57,"y1":0,"x2":1.57,"y2":func09(1.57),"stroke":"#ff0","opacity":0.8},
    {"x1":0,"y1":func09(1.57),"x2":1.57,"y2":func09(1.57),"stroke":"#ff0","opacity":0.8},
    {"x1":3.14,"y1":0,"x2":3.14,"y2":func09(3.14),"stroke":"#0ff","opacity":0.8},
    {"x1":0,"y1":func09(3.14),"x2":3.14,"y2":func09(3.14),"stroke":"#0ff","opacity":0.8},
  ];
  drawLine(svg09,lineData09,xScale09,yScale09);
  drawLine(svg091,lineData09,xScale09,yScale09);

  // circle
  var circleData09 = [
    {"cx":3.14/2,"cy":func09(3.14/2),"r":2,"stroke":"#ff0","fillColor":"#ff0"},
    {"cx":3.14,"cy":func09(3.14),"r":2,"stroke":"#0ff","fillColor":"#0ff"}
  ];
  drawCircle(svg09,circleData09,xScale09,yScale09);
  // circle
  circleData091 = [
    {"cx":3.14/2,"cy":func09(3.14/2),"r":3,"stroke":"#fff","fillColor":"#333"},
    {"cx":3.14,"cy":func09(3.14),"r":3,"stroke":"#fff","fillColor":"#333"}
  ];
  drawCircle(svg091,circleData091,xScale09,yScale09);

  // mathjax
  foData09 = [
    {"x":0.4,
    "y":0.7,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":3.8,
    "y":0.7,
    "text":"$$b$$",
    "fontSize":"18px"},
    {"x":1.56,
    "y":0.7,
    "text":"$$c$$",
    "fontSize":"18px"},
    {"x":3.13,
    "y":0.7,
    "text":"$$d$$",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":1.3,
    "text":"$$f(c)$$",
    "fontSize":"16px"},
    {"x":-0.5,
    "y":5.3,
    "text":"$$f(d)$$",
    "fontSize":"16px"}
  ];

  drawMathjax(svg09,foData09,xScale09,yScale09);
  drawMathjax(svg091,foData09,xScale09,yScale09);

  // lines
  lineData092 = [
    {"x1":0.5,"y1":1,"x2":4,"y2":4,"stroke":"#fff"},
    {"x1":0.5,"y1":1,"x2":0.5,"y2":0,"stroke":"#f0f","opacity":0.6},
    {"x1":0,"y1":1,"x2":0.5,"y2":1,"stroke":"#f0f","opacity":0.8},
    {"x1":4,"y1":0,"x2":4,"y2":4,"stroke":"#0ff","opacity":0.8},
    {"x1":0,"y1":4,"x2":4,"y2":4,"stroke":"#0ff","opacity":0.8},
  ];
  drawLine(svg092,lineData092,xScale09,yScale09);
  circleData092 = [
    {"cx":0.5,"cy":1,"r":3,"stroke":"#fff","fillColor":"#333"},
    {"cx":4,"cy":4,"r":3,"stroke":"#fff","fillColor":"#333"}
  ];
  drawCircle(svg092,circleData092,xScale09,yScale09);

  // mathjax
  foData092 = [
    {"x":0.4,
    "y":0.7,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":3.9,
    "y":0.7,
    "text":"$$b$$",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":2.0,
    "text":"$$f(a)$$",
    "fontSize":"16px"},
    {"x":-0.5,
    "y":5.0,
    "text":"$$f(b)$$",
    "fontSize":"16px"}
  ];

  drawMathjax(svg092,foData092,xScale09,yScale09);

  // Relative minima and maxima
  var xScale10 = d3.scale.linear()
                       .domain([-1,10])
                       .range([50,450]);

  var yScale10 = d3.scale.linear()
                       .domain([10,-1])
                       .range([50,450]);

  // 軸
  axesData10 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale10,
    "yScale":yScale10
  };
  drawAxes(svg10,axesData10);

  var pathData10 =[];
  function func10(i){
    return (-Math.pow(i,3)*7+107*i*i-481*i+813)/48;
  }
  for (var i=1;i<=9;i=i+0.1){
    pathData10.push(new Point(i,func10(i)));
  };
  drawPath(svg10,pathData10,{"stroke":"#fff"},xScale10,yScale10);

  // lines
  lineData10 = [
  {"x1":1,"y1":0,"x2":1,"y2":9,"stroke":"#f0f","opacity":0.6},
  {"x1":0,"y1":9,"x2":1,"y2":9,"stroke":"#f0f","opacity":0.8},
  {"x1":9,"y1":0,"x2":9,"y2":1,"stroke":"#0ff","opacity":0.8},
  {"x1":0,"y1":1,"x2":9,"y2":1,"stroke":"#0ff","opacity":0.8},
  {"x1":3.3,"y1":0,"x2":3.3,"y2":2.9,"stroke":"#ff0","opacity":0.8},
  {"x1":0,"y1":2.9,"x2":3.3,"y2":2.9,"stroke":"#ff0","opacity":0.8},
  {"x1":6.9,"y1":0,"x2":6.9,"y2":6,"stroke":"#ff0","opacity":0.8},
  {"x1":0,"y1":6,"x2":6.9,"y2":6,"stroke":"#ff0","opacity":0.8},
  ];
  drawLine(svg10,lineData10,xScale10,yScale10);

  // mathjax
  foData10 = [
  {"x":0.9,
  "y":1,
  "text":"$$a$$",
  "fontSize":"18px"},
  {"x":8.9,
  "y":1,
  "text":"$$b$$",
  "fontSize":"18px"},
  {"x":3.2,
  "y":1,
  "text":"$$c$$",
  "fontSize":"18px"},
  {"x":6.8,
  "y":1,
  "text":"$$d$$",
  "fontSize":"18px"},
  {"x":-1,
  "y":10.5,
  "text":"$$f(a)$$",
  "fontSize":"16px"},
  {"x":-1,
  "y":2.5,
  "text":"$$f(b)$$",
  "fontSize":"16px"},
  {"x":-1,
  "y":4.5,
  "text":"$$f(c)$$",
  "fontSize":"16px"},
  {"x":-1,
  "y":7.5,
  "text":"$$f(d)$$",
  "fontSize":"16px"},
  {"x":8.9,
  "y":5,
  "text":"$$f(x)$$",
  "fontSize":"16px"}
  ];

  drawMathjax(svg10,foData10,xScale10,yScale10);

  /** CONCAVITY **/
  var xScale11 = d3.scale.linear()
  .domain([-1,8])
  .range([50,450]);

  var yScale11 = d3.scale.linear()
  .domain([10,-10])
  .range([50,450]);
  // 軸
  axesData11 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale11,
    "yScale":yScale11
  };

  drawAxes(svg11,axesData11);
  var pathData11_1 =[];
  var pathData11_2 =[];
  var pathData11_3 =[];
  function func11_1(i){
    return Math.pow(i,3)/3-4*i*i+10*i+4;
  }
  function func11_2(i){
    return Math.pow(i,2)-8*i+10;
  }
  function func11_3(i){
    return 2*i-8;
  }

  for (var i=0;i<=8;i=i+0.1){
    pathData11_1.push(new Point(i,func11_1(i)));
  };
  drawPath(svg11,pathData11_1,{"stroke":"#fff"},xScale11,yScale11);
  for (var i=0;i<=8;i=i+0.1){
    pathData11_2.push(new Point(i,func11_2(i)));
  };
  drawPath(svg11,pathData11_2,{"stroke":"#f0f"},xScale11,yScale11);

  for (var i=0;i<=8;i=i+0.1){
    pathData11_3.push(new Point(i,func11_3(i)));
  };
  drawPath(svg11,pathData11_3,{"stroke":"#0f0"},xScale11,yScale11);

  lineData11 = [
    {"x1":4-Math.sqrt(6),"y1":0,
     "x2":4-Math.sqrt(6),"y2":func11_1(4-Math.sqrt(6)),
     "stroke":"#f0f","opacity":0.5},
    {"x1":4+Math.sqrt(6),"y1":0,
     "x2":4+Math.sqrt(6),"y2":func11_1(4+Math.sqrt(6)),
     "stroke":"#f0f","opacity":0.5},
  ]
  drawLine(svg11,lineData11,xScale11,yScale11);

  circleData11 = [
    {"cx":4-Math.sqrt(6),"cy":func11_1(4-Math.sqrt(6)),
     "r":3,"stroke":"#ff0","fillColor":"#ff0"},
    {"cx":4+Math.sqrt(6),"cy":func11_1(4+Math.sqrt(6)),
     "r":3,"stroke":"#ff0","fillColor":"#ff0"},
  ]
  drawCircle(svg11,circleData11,xScale11,yScale11);

  // mathjax
  foData11 = [
  {"x":0.9,
  "y":-3.3,
  "text":"$$f''(x)$$",
  "fontSize":"18px"},
  {"x":3.2,
  "y":11.5,
  "text":"$$f(x)$$",
  "fontSize":"16px"},
  {"x":7,
  "y":5,
  "text":"$$f'(x)$$",
  "fontSize":"16px"}
  ];

  drawMathjax(svg11,foData11,xScale11,yScale11);

  /** An inflection point **/
  drawAxes(svg12,axesData11);
  drawPath(svg12,pathData11_1,{"stroke":"#fff"},xScale11,yScale11);
  drawPath(svg12,pathData11_2,{"stroke":"#f0f"},xScale11,yScale11);
  drawPath(svg12,pathData11_3,{"stroke":"#0f0"},xScale11,yScale11);
  lineData12 = [
    {"x1":4,"y1":0,
     "x2":4,"y2":func11_1(4),
     "stroke":"#f0f","opacity":0.5},
    {"x1":4,"y1":0,
     "x2":4,"y2":func11_2(4),
     "stroke":"#f0f","opacity":0.5},
  ]
  drawLine(svg12,lineData12,xScale11,yScale11);
  circleData12 = [
    {"cx":4,"cy":func11_1(4),
     "r":3,"stroke":"#ff0","fillColor":"#ff0"},
  ]

  drawCircle(svg12,circleData12,xScale11,yScale11);
  drawMathjax(svg12,foData11,xScale11,yScale11);

  /**
    OPTIMIZATION WITH CALCULUS
  **/

  lineData131 = [
    // corner boxes 
    {"x1":100,"y1":50,
     "x2":100,"y2":100,
     "stroke":"aqua","opacity":0.5},
    {"x1":50,"y1":100,
     "x2":100,"y2":100,
     "stroke":"aqua","opacity":0.5},
    {"x1":300,"y1":50,
     "x2":300,"y2":100,
     "stroke":"aqua","opacity":0.5},
    {"x1":350,"y1":100,
     "x2":300,"y2":100,
     "stroke":"aqua","opacity":0.5},
    {"x1":100,"y1":250,
     "x2":100,"y2":200,
     "stroke":"aqua","opacity":0.5},
    {"x1":50,"y1":200,
     "x2":100,"y2":200,
     "stroke":"aqua","opacity":0.5},
    {"x1":300,"y1":250,
     "x2":300,"y2":200,
     "stroke":"aqua","opacity":0.5},
    {"x1":350,"y1":200,
     "x2":300,"y2":200,
     "stroke":"aqua","opacity":0.5},
  ]
  drawLine(svg131,lineData131);
  rectData131 = [
    {"x":50,"y":50,"width":300,"height":200,"stroke":"#fff"}
   ,{"x":100,"y":100,"width":200,"height":100,"stroke":"gold"}
  ]
  drawRect(svg131,rectData131);

  // mathjax
  foData131 = [
  {"x":180,
  "y":-25,
  "text":"$$30cm$$",
  "fontSize":"16px"},
  {"x":0,
  "y":100,
  "text":"$$20cm$$",
  "fontSize":"16px"},
  {"x":110,
  "y":15,
  "text":"$$x$$",
  "fontSize":"16px"},
  {"x":70,
  "y":50,
  "text":"$$x$$",
  "fontSize":"16px"},
  {"x":110,
  "y":165,
  "text":"$$x$$",
  "fontSize":"16px"},
  {"x":70,
  "y":130,
  "text":"$$x$$",
  "fontSize":"16px"},
  
  {"x":280,
  "y":15,
  "text":"$$x$$",
  "fontSize":"16px"},
  {"x":320,
  "y":50,
  "text":"$$x$$",
  "fontSize":"16px"},
  {"x":280,
  "y":165,
  "text":"$$x$$",
  "fontSize":"16px"},
  {"x":320,
  "y":130,
  "text":"$$x$$",
  "fontSize":"16px"},
  ];

  drawMathjax(svg131,foData131);

  lineData132 = [
    {"x1":200,"y1":250,"x2":200,"y2":200,"stroke":"#fff"},
    {"x1":350,"y1":230,"x2":350,"y2":185,"stroke":"#fff"},
    {"x1":50,"y1":130,"x2":50,"y2":90,"stroke":"#fff"},
    {"x1":190,"y1":110,"x2":190,"y2":75,"stroke":"#fff"},
    {"x1":200,"y1":200,"x2":350,"y2":185,"stroke":"#fff"},
    {"x1":200,"y1":250,"x2":350,"y2":230,"stroke":"#fff"},
    {"x1":200,"y1":200,"x2":50,"y2":90,"stroke":"#fff"},
    {"x1":200,"y1":250,"x2":50,"y2":130,"stroke":"#fff"},
    {"x1":50,"y1":90,"x2":190,"y2":75,"stroke":"#fff"},
    {"x1":190,"y1":75,"x2":350,"y2":185,"stroke":"#fff"},
    {"x1":190,"y1":110,"x2":302,"y2":191,"stroke":"#fff"},
    {"x1":96,"y1":124,"x2":190,"y2":110,"stroke":"#fff"},

  ]
  drawLine(svg132,lineData132);

  // mathjax
  foData132 = [
  {"x":210,
  "y":165,
  "text":"$$x$$",
  "fontSize":"16px"},
  
  {"x":250,
  "y":200,
  "text":"$$20-2x$$",
  "fontSize":"16px"},

  {"x":250,
  "y":50,
  "text":"$$30-2x$$",
  "fontSize":"16px"}
  ];

  drawMathjax(svg132,foData132);

  /** IN DIFFERENT FIELDS**/
  var xScale14 = d3.scale.linear()
  .domain([0,400])
  .range([50,450]);

  var yScale14 = d3.scale.linear()
  .domain([10000,0])
  .range([50,450]);
  // 軸
  axesData14 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale14,
    "yScale":yScale14
  };

  drawAxes(svg14,axesData14);
  var pathData14 =[];
  function func14(i){
    return 3200+0.1*i-0.001*Math.pow(i,2) + 0.0004*Math.pow(i,3);
  }
  function slope14(i){
    return 0.1-0.002*i + 0.0012*Math.pow(i,2);
  }

  for (var i=0;i<=400;i=i+1){
    pathData14.push(new Point(i,func14(i)));
  };
  drawPath(svg14,pathData14,{"stroke":"#fff"},xScale14,yScale14);

  circleData14 = [
    {"cx":100,"cy":func14(100),
     "r":3,"stroke":"#ff0","fillColor":"#ff0"},
  ]

  drawCircle(svg14,circleData14,xScale14,yScale14);

  lineData14 = [
    {"x1":200,"y1":func14(100)+slope14(100)*100,
    "x2":0,"y2":func14(100)-slope14(100)*100,"stroke":"#f0f"}
  ];

  drawLine(svg14,lineData14,xScale14,yScale14);

  // mathjax
  foData14 = [
  {"x":350,
  "y":600,
  "text":"$$quantity$$",
  "fontSize":"16px"},
  
  {"x":-10,
  "y":12000,
  "text":"$$cost(q)$$",
  "fontSize":"16px"},

  ];

  drawMathjax(svg14,foData14,xScale14,yScale14);

  /** Mean value theorem */
  var xScale15 = d3.scale.linear()
  .domain([0,10])
  .range([50,450]);

  var yScale15 = d3.scale.linear()
  .domain([60,0])
  .range([50,450]);
  // 軸
  axesData15 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale15,
    "yScale":yScale15
  };

  drawAxes(svg15,axesData15);
  var pathData15 =[];
  function func15(i){
    return 20 -16 * i + 6*Math.pow(i,2) - 0.45*Math.pow(i,3);
  };
  function slope15(i){
    return -16 + 12*i - 1.35 * Math.pow(i,2);
  }

  for (var i=1;i<=9;i=i+0.01){
    pathData15.push(new Point(i,func15(i)));
  };
  drawPath(svg15,pathData15,{"stroke":"#fff"},xScale15,yScale15);

  lineData15 = [
    {"x1":1,"y1":func15(1),"x2":1,"y2":0,"stroke":"#0f0","opacity":0.4}
   ,{"x1":0,"y1":func15(1),"x2":9,"y2":func15(1),"stroke":"#0f0","opacity":0.4}
   ,{"x1":9,"y1":func15(9),"x2":9,"y2":0,"stroke":"#0f0","opacity":0.4}
   ,{"x1":9,"y1":func15(9),"x2":0,"y2":func15(9),"stroke":"#0f0","opacity":0.4}
   ,{"x1":2.07,"y1":func15(2.07),"x2":2.07,"y2":0,"stroke":"#0f0","opacity":0.4}
   ,{"x1":6.82,"y1":func15(6.82),"x2":6.82,"y2":0,"stroke":"#0f0","opacity":0.4}
   //secant
   ,{"x1":1,"y1":func15(1),"x2":9,"y2":func15(9),"stroke":"#f0f"}
   // tangent
   ,{"x1":1.07,"y1":func15(2.07)-slope15(2.07),
   "x2":3.07,"y2":slope15(2.07)+func15(2.07),"stroke":"#ff0"}
   ,{"x1":5.82,"y1":func15(6.82)-slope15(6.82),
   "x2":7.82,"y2":slope15(6.82)+func15(6.82),"stroke":"#ff0"}
  ]
  drawLine(svg15,lineData15,xScale15,yScale15);

  // mathjax
  foData15 = [
  {"x":10.5,
  "y":5,
  "text":"$$x$$",
  "fontSize":"16px"},
  
  {"x":-1,
  "y":70,
  "text":"$$y$$",
  "fontSize":"16px"},

  {"x":0.9,
  "y":5,
  "text":"$$a$$",
  "fontSize":"16px"},
  {"x":8.9,
  "y":5,
  "text":"$$b$$",
  "fontSize":"16px"},
  {"x":2,
  "y":5,
  "text":"$$c1$$",
  "fontSize":"16px"},
  {"x":6.5,
  "y":5,
  "text":"$$c2$$",
  "fontSize":"16px"},

  {"x":-1,
  "y":19,
  "text":"$$f(a)$$",
  "fontSize":"16px"},
  {"x":-1,
  "y":43,
  "text":"$$f(b)$$",
  "fontSize":"16px"},
  {"x":9,
  "y":50,
  "text":"$$f(x)$$",
  "fontSize":"16px"},

  ];

  drawMathjax(svg15,foData15,xScale15,yScale15);

  /** */
  var xScale16 = d3.scale.linear()
  .domain([0,7])
  .range([50,450]);

  var yScale16 = d3.scale.linear()
  .domain([5,-2])
  .range([50,450]);
  // 軸
  axesData16 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[2,3.5,5],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale16,
    "yScale":yScale16
  };

  drawAxes(svg16,axesData16);
  var pathData16 =[];
  function func16(i){
    return 8 -6*i + Math.pow(i,2);
  };
  function slope16(i){
    return -6 + 2*i;
  }

  for (var i=2;i<=5;i=i+0.01){
    pathData16.push(new Point(i,func16(i)));
  };
  drawPath(svg16,pathData16,{"stroke":"#fff"},xScale16,yScale16);

  lineData16 = [
    {"x1":2,"y1":func16(2),"x2":5,"y2":func16(5),"stroke":"#f0f"}
   ,{"x1":2.5,"y1":func16(3.5)-slope16(3.5),
   "x2":4.5,"y2":func16(3.5)+slope16(3.5),"stroke":"#0f0"}
  ]
  drawLine(svg16,lineData16,xScale16,yScale16);

  /** Local linearization */
  var xScale17 = d3.scale.linear()
  .domain([3.9,4.5])
  .range([50,450]);

  var yScale17 = d3.scale.linear()
  .domain([2.12,1.99])
  .range([50,450]);

  var pathData17 =[];
  function func17(i){
    return Math.sqrt(i);
  };
  function slope17(i){
    return Math.pow(i,-1/2)/2;
  }

  for (var i=0;i<=5;i=i+0.01){
    pathData17.push(new Point(i,func17(i)));
  };
  drawPath(svg17,pathData17,{"stroke":"#fff"},xScale17,yScale17);

  lineData17 = [
   {"x1":3,"y1":func17(4)-slope17(4),
   "x2":5,"y2":func17(4)+slope17(4),"stroke":"#f0f"}
  ]
  drawLine(svg17,lineData17,xScale17,yScale17);

  circleData17 = [
    {"cx":4,"cy":func17(4),"r":2,"stroke":"#fff","fillColor":"#fff"}
   ,{"cx":4.36,"cy":func17(4)+slope17(4)*0.36,"r":2,"stroke":"#fff","fillColor":"#fff"}
  ];

  drawCircle(svg17,circleData17,xScale17,yScale17);

  // mathjax
  foData17 = [
  {"x":4,
  "y":2.01,
  "text":"$$(4,f(4))$$",
  "fontSize":"16px"},
  
  {"x":4.1,
  "y":2.11,
  "text":"$$(4.36,L(4.36))$$",
  "fontSize":"16px"},

  ];

  drawMathjax(svg17,foData17,xScale17,yScale17);


</script>
