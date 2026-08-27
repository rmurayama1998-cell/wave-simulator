# 波のシミュレーション（参考作成版）

他サイトのシミュレーションを参考に、あらためて作りなおしたものです。
本体（`../`）にある自作ツールとは分けて、このフォルダにまとめています。

インストール不要・ログイン不要。外部リソースに依存しない単一のHTMLなので、一度読み込めばオフラインでも動きます。横向きの画面で使ってください。

## 公開URLと QRコード

トップページ（3つへのリンク集）

| | |
|---|---|
| URL | https://rmurayama1998-cell.github.io/wave-simulator/remake/ |
| QRコード | `qr-remake-top.png` |

### ① 進行波の波形 — `traveling.html`

パルスや連続波が右へ進むようすを見せるツールです。

- 波形1／波形2：手が1回振って、半波長のパルスが右へ進む（上向き・下向き）
- 波形3：振り続けて、5波長の波列が通り過ぎる
- 連続波：途切れない正弦波
- 緑球／赤球／青球／赤･青球：媒質の位置に玉を置く（赤はλごと、青はλ/2ずれた位置）
- 波長 −＋／振動数 −＋：λ（200〜1200）と周期 T（16〜3の8段階）を変更。速さ v = fλ は自動で決まります

| | |
|---|---|
| URL | https://rmurayama1998-cell.github.io/wave-simulator/remake/traveling.html |
| QRコード | `qr-traveling.png` |

### ② 波と媒質の振動 — `oscillation.html`

上に y–x グラフ（波形そのもの）、下に y–t グラフ（選んだ媒質1点の変位の記録）を並べます。波がその点を通り過ぎると、その点の上下運動が下のグラフにペンで描かれていきます。

- 媒質１〜４：注目する点を λ/4 ずつずらして選ぶ
- スタート：波を動かし始める
- パルス波／正弦波／連続波：波の来かたを変える
- 振幅反転：波の山と谷を上下逆にする

横方向の目盛りは2つのグラフでそろえてあるので、波長と周期を同じ長さで見比べられます。

| | |
|---|---|
| URL | https://rmurayama1998-cell.github.io/wave-simulator/remake/oscillation.html |
| QRコード | `qr-oscillation.png` |

### ③ 波の合成と定常波 — `composite-wave.html`

左から進む波（青）と右から進む波（赤）を重ね合わせ、その和である合成波（緑）を描きます。

- パルス１（正弦の山）／パルス２（く形波）：2つのパルスがすれ違う
- 正弦波／進行波：先端のある波、または最初から続いている波
- 定常波：腹（赤玉）と節（青玉）の目印つき
- 合成波／入射波／入射波･合成波：表示の切り替え
- 同位相／逆位相：右から来る波の山と谷をひっくり返す

く形波は、ぴったり重なった瞬間に合成波が同位相でちょうど2倍、逆位相でちょうど0になります。

| | |
|---|---|
| URL | https://rmurayama1998-cell.github.io/wave-simulator/remake/composite-wave.html |
| QRコード | `qr-composite-wave.png` |

## 参考にしたサイト

構成・操作の流れは [物理シミュレーション（physics.cloudfree.jp）](https://physics.cloudfree.jp/) の以下のページを参考にしました。コードはすべて新たに書き起こしたもので、画像などの素材は使用していません（描画はすべて HTML5 Canvas）。

| 本フォルダ | 参考にしたページ |
|---|---|
| `traveling.html` | https://physics.cloudfree.jp/main/osci_wave/shinkouha-hakei5-m/index.html |
| `oscillation.html` | https://physics.cloudfree.jp/main/osci_wave/shinkouha-shindou2-m/index.html |
| `composite-wave.html` | https://physics.cloudfree.jp/main/osci_wave/gousei2-m/index.html |

元サイトから変えた主な点

- 配色を生成り色の背景・黒い座標軸にし、プロジェクター投影と動画の切り抜きに向くようにした
- 画面の高さを基準に拡大し、横は入るぶんだけ軸を伸ばす方式にした（画面の形が変わっても波の形＝振幅と波長の比が変わらない）
- 軸の先端（矢印）の外側に余白を設けた
- `traveling.html` に波長・振動数を変えるボタンを追加した
- `composite-wave.html` の定常波の腹・節が、画面幅によらず必ず目盛り線の上に来るようにした
