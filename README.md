# beginner-fashion-mnist-competition

Fashion-MNIST を使ったシンプルな分類モデルのデモ用リポジトリです。

## コンペ概要

- 開催期間: 2026/6/7 ~ 2026/6/14
- 評価対象: `uv run src/submit.py` 実行時に表示される `Test Accuracy`
- 注意事項: 上位者には、学習スクリプト等の追加提出を依頼し、再現性を確認する場合があります

## 動作環境

- Python 3.12 以上
- `uv` インストール済み

依存関係は `pyproject.toml` で管理されています。

## 使い方

以下はリポジトリのルートで実行してください。

### 1. データセットのダウンロード

```bash
uv run src/download_fashion_mnist.py
```

`data/` 配下に Fashion-MNIST の 4 ファイルが保存されます。

### 2. 学習して pkl を作成

```bash
uv run src/train.py
```

学習後、ルートに `sample_weight.pkl` が作成されます。

### 3. submit.py で評価

```bash
uv run src/submit.py
```

`sample_weight.pkl` を読み込み、テストデータに対する `Test Accuracy` を表示します。

## 主要ファイル

- `src/download_fashion_mnist.py`: Fashion-MNIST のダウンロード
- `src/load_fashion_mnist.py`: データ読み込み（train/valid/test 分割）
- `src/network.py`: シンプルな MLP ネットワーク定義
- `src/train.py`: 学習して pkl を保存
- `src/submit.py`: pkl を読み込み精度を出力

## 提出方法

最新のリポジトリリンクを `@osawakousei_09490` へ DM で送付してください。

提出内容は以下です。

- モデルの pkl ファイル
- `submit.py` および `uv run src/submit.py` で動作させるために必要な依存ファイル

補足:

- `uv` はインストール済み環境を前提とします
- 必要に応じて再現確認のため追加ファイル提出をお願いする場合があります
