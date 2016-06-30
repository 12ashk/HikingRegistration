# HikingRegistration
登山計画書作成支援用LaTeXスタイルファイル

## コースタイムの入力支援
``` LaTeX
\usepackage{coursetime.sty}
```
とプリアンブルに記入して利用してください．

### 予定コースタイムの入力
行動開始時刻と，歩行時間・行き先，休憩時間を指定すれば，自動的に予定コースタイムを入力できます．

例えば
``` LaTeX
A登山口 \ctset{6}{00}
\ctwalk{45}{B峠}
\ctrest{10}
\ctwalk{70}{C山}
\ctrest{10}
\ctwalk{20}{D山}
```
と入力すれば
``` 
A登山口 6:00 -(45 min)- B峠 6:45 ~ 6:55 - (70 min) - C山 8:05 ~ 8:15 - (20 min) - D山 8:35
```
といった出力が得られます．

### 交通機関の入力
交通機関や自動車を用いた移動については\cttran{所要時間}{目的地}{交通手段}というコマンドを使ってください．
``` LaTeX
東京駅 \ctset{6}{30}
\cttran{120}{熱海駅}{JR東海道線}
```
とすれば
``` LaTeX
東京駅 6:30 - [JR東海道線,120min] - 熱海駅 8:30
```
という出力が得られます．