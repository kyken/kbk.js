# kbk.js


## abstract

stockの4本値に対してトレンド分析を行い、分析のヒストリカルな評価から現在の投資判断を提示するアプリケーション


## design

### component

以下のコンポーネントで構成されるモノリポである

- crawler: 株価データを取得するモジュール
- core: トレンドの分析と評価を行うためのモジュール
- ui: 投資判断を表示するモジュール

#### crawler

ソースを指定して株価の4本値の情報を溜め込むことを責務とするモジュール
取得する部分と溜め込む部分の分離くらいを気にしたいところs

#### core

`crawler`で溜め込んだ各銘柄の4本値をもとに、種々のトレンド分析指標ごとに以下を行う
- 過去から現在までにおけるバックテストの計算と評価
- リアルタイムの投資判断の提示

#### ui

`core`で計算した投資判断を綺麗に見せる（趣味）



