# slot-heatmap

パチスロホールの台ごとの**差枚データをヒートマップ表示するスマホ対応Webアプリ**です。  
CSVファイルをアップロードするだけで、ホールのフロアマップに「台番号・機種名・差枚数」を正方形セルで自動描画し、PNG形式で保存できます。

> **Smartphone-friendly heatmap viewer for Japanese pachislot machine performance (win/loss) data.**  
> Upload floor & delta CSVs → visualize differences in a grid layout → export as PNG.

---

## 機能 / Features

- [x] 台配置CSV + 差枚CSVをアップロードしてマップを生成
- [x] **1台 = 正方形セル**に3行表示（台番号・機種名・差枚）
- [x] 差枚がプラスの台のみ色分け（1,000枚ごとに5段階）
- [x] スマホ縦画面に最適化（ピンチズーム、横スクロール対応）
- [x] PNG画像として保存（iOS・Android両対応）
- [x] 完全クライアントサイド処理（サーバー不要）

---

## デモ
https://ttettettett.github.io/slot-heatmap/

（GitHub Pages にデプロイするだけですぐ使えます）

---

## 使い方 / Usage

1. `floor_map.csv`（ホールの台配置）と `sama_data.csv`（差枚データ）を用意
2. 画面上の **「フロアCSV」「差枚CSV」** ボタンからそれぞれ選択
3. 自動でヒートマップが表示されます
4. **PNG保存ボタン**で画像として出力できます

### CSVフォーマット

#### フロアCSV（カンマ区切り）

```csv
1,2,,3,,4
,,,,,
5,,6,7,,8
