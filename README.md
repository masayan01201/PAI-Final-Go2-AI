PAI Final Project - Go2 AI Posture Control
Overview
Google ColabとGenesisを使用して、 Unitree Go2の姿勢制御を検証した最終課題です。

Random Forestを用いて、 以下の2つを入力しました。

Posture level
Motion speed
AIから以下を推論しています。

12 joint angles
Body height
Transition steps
Training
5 posture levels × 3 speed levels = 15 training conditions

Unseen conditions
以下の未学習条件でも推論を行いました。

Posture 0.35 / Speed 0.25
Posture 0.55 / Speed 0.70
Posture 0.85 / Speed 0.40
Improvement
AI出力をそのまま適用すると脚が浮いて見える場合があったため、 calfリンク高さを基準とした近似補正を追加しました。

Reference calf-link Z = 0.107 m

最大8回の補正を行っています。

Notes
教師データは人工的に作成したデータです。

calfリンク高さによる補正は、 実際の足裏接触や接触力を保証するものではありません。
