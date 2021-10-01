# math-tools

## toolのリンク

  - [Wolfram|Alpha](https://ja.wolframalpha.com/)
  - [gnuplot](http://www.gnuplot.info/)
  - [MathLibre](http://www.mathlibre.org/index-ja.html)
    - [Rufus](https://rufus.ie/ja/)
  - [GeoGebra](https://www.geogebra.org/?lang=ja)
  - [LaTex](https://ja.wikipedia.org/wiki/LaTeX)
  - [GRAPES](https://grapes-light.app/app)

## gnuplotで使うコード

```c
# gnuplotの初期設定
reset # 初期化
set term gif animate delay 1 # アニメ化

set xrange [-5:5] # xの定義域
set yrange [-5:5] # yの定義域
set size square # グラフを正方形に

# x-y軸の表示
set xzeroaxis
set yzeroaxis

# 出力データの名前
set output "graph_anime.gif"

# グラフタイトル用
titleStr(n) = sprintf("y=%2.2f*x**2",n)
# ----------------------------------
# 描画用
do for [i=-50:50]{
  a=i*0.04 # aは-2～2
  plot a*x**2 title titleStr(a)
}

# 出力
set output
```
