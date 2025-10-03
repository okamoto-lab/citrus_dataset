# 柑橘推薦データセット
このリポジトリでは，以下のデータセットを公開しています．
- `citrus_user_rating.tsv`
- `citrus_features.tsv`

本データは，柑橘の嗜好調査および品種特性の整理を目的に収集・作成されたものであり，推薦システムや食品嗜好研究における教育・研究利用を想定しています．

両方のデータセットに含まれるスコアは1〜6の6段階評価で設定されています．また，item_idは両データ間を結ぶ外部キーとして機能します．これにより，ユーザ官能評価データと品種特徴データを結合して利用できます．


## ファイル形式
- 形式: TSV (Tab Separated Values)
- 文字コード: UTF-8
- 区切り文字: タブ（`\t`）


## 各ファイルの内容

### 1. `citrus_user_rating.tsv`
柑橘類におけるユーザ官能評価データ．

| カラム名 | データ型 | 説明 |
|----------|----------|------|
| user_id    | Integer | 評価者ID（匿名化済み） |
| item_id    | Integer | 柑橘品種ID（外部キー） |
| item_name  | String  | 柑橘品種名 |
| brix       | Integer | 甘味の評価スコア（1〜6）|
| acid       | Integer | 酸味の評価スコア（1〜6）|
| bitter     | Integer | 苦味の評価スコア（1〜6）|
| smell      | Integer | 香りの評価スコア（1〜6）|
| moisture   | Integer | 水分量の評価スコア（1〜6）|
| elastic    | Integer | 弾力の評価スコア（1〜6）|
| overall    | Integer | 総合的な評価スコア（1〜6）|

---

### 2. `citrus_features.tsv`
柑橘品種の特徴データ．

| カラム名 | データ型 | 説明 |
|----------|----------|------|
| item_id     | Integer | 柑橘品種ID （外部キー）|
| item_name   | String  | 柑橘品種名 |
| brix        | Integer | 甘味の特徴スコア（1〜6） |
| acid        | Integer | 酸味の特徴スコア（1〜6） |
| bitter      | Integer | 苦味の特徴スコア（1〜6） |
| smell       | Integer | 香りの特徴スコア（1〜6） |
| moisture    | Integer | 水分量の特徴スコア（1〜6） |
| elastic     | Integer | 弾力の特徴スコア（1〜6） |


## 引用のお願い
研究等で利用された場合は，以下の論文を引用いただけますと幸いです．

```bibtex
@inproceedings{k.hosoo_2025,
  title = {柑橘類を対象とした推薦システムの実現に向けた基礎的調査},
  author = {細尾 佳意 and 岡本 一志 and 原田 慧 and 柴田 淳司 and 軽部 幸起},
  booktitle = {第39回人工知能学会全国大会論文集},
  pages = {1Win483-1Win483},
  year = {2025},
  doi = {10.11517/pjsai.JSAI2025.0_1Win483}
}
```

## 参考文献
- mikan-note（柑橘ソムリエ）：みかん図鑑，2024.
  https://booth.pm/ja/items/5977950
- 伊藤農園：みかんな図鑑，
  https://www.ito-noen.com/dictionary/
- 広井亜香里：柑橘の教科書，大成社，2020.


## 謝辞
本データセットの作成に協力いただいた参加者，柑橘農家の皆様に感謝いたします．


## 更新履歴
- 2025-10-01: 初版公開
