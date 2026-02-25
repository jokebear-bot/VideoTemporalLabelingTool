# ビデオ時間ラベリングツール

[English](README.md) | [中文](README.zh.md) | [日本語](README.ja.md)

wxPython ベースの GUI アプリケーションによるビデオ時間ラベリングツール。ビデオの時間ラベルを記録し、対応する開始フレームと終了フレームのインデックスを保存します。

![UI](./UI.png)

## 機能

- 🎥 複数のビデオ形式をサポート（.avi, .mp4, .mov, .mkv, .wav）
- 🏷️ 開始/終了フレーム選択による時間ラベリング
- 🎯 複数のアクションタイプ（トリッピング、フェイスオフ、カスタマイズ可能）
- 📐 ショットタイプ分類（クローズ、ミッド、ファー）
- ⚡ 調整可能なフレームステップ間隔（5, 10, 15, 20, 30 FPS）
- 💾 ラベルデータの CSV エクスポート
- 🖥️ クロスプラットフォーム対応（Windows, macOS, Linux）

## 必要条件

- Python >= 3.9（推奨：3.12 LTS）
- wxPython >= 4.2.0
- pandas >= 2.0.0
- opencv-python >= 4.9.0
- numpy >= 1.24.0

## インストール

### PyPI から（近日公開）

```bash
pip install vtlt
```

### ソースから

```bash
# リポジトリをクローン
git clone https://github.com/jokebear-bot/VideoTemporalLabelingTool.git

# ディレクトリに移動
cd VideoTemporalLabelingTool

# 依存関係をインストール
pip install -r requirements.txt

# またはパッケージとしてインストール
pip install -e .
```

## クイックスタート

### 直接実行

```bash
# ソースから実行
python -m vtlt

# またはエントリポイントを使用（pip インストール後）
vtlt
```

### 使用方法

1. **データセットパスの設定**: ビデオデータセットディレクトリのパスを入力
2. **保存パスの設定**: ラベルが保存されるパスを入力
3. **ビデオの選択**: 前/次ボタンでビデオを切り替え
4. **フレームのナビゲーション**: +/- ボタンまたは FPI（フレーム毎間隔）で移動
5. **開始/終了のマーク**: 「開始」「終了」ボタンで時間的境界をマーク
6. **タイプの選択**: ショットタイプを選択（クローズ/ミッド/ファー）
7. **ラベルの保存**: 「保存」ボタンでラベルを CSV に保存

## プロジェクト構造

```
VideoTemporalLabelingTool/
├── src/
│   └── vtlt/
│       ├── __init__.py      # パッケージ初期化
│       ├── app.py           # GUI アプリケーション
│       ├── service.py       # ビジネスロジック
│       └── resource/        # リソースファイル
├── tests/                   # 単体テスト
├── requirements.txt         # 依存関係
├── pyproject.toml          # プロジェクト設定
├── README.md               # 英語ドキュメント
└── CHANGELOG.md            # バージョン履歴
```

## 開発

### 開発環境のセットアップ

```bash
# 開発依存関係をインストール
pip install -e ".[dev]"

# テストを実行
pytest

# コードをフォーマット
black src/
ruff check src/

# 型チェック
mypy src/
```

### パッケージのビルド

```bash
python -m build
```

## 互換性

| Python バージョン | 状態 |
|----------------|------|
| 3.9 | ✅ サポート済み |
| 3.10 | ✅ サポート済み |
| 3.11 | ✅ サポート済み |
| 3.12 | ✅ 推奨（LTS）|

## 変更履歴

[CHANGELOG.md](CHANGELOG.md) を参照してください。

## ライセンス

このプロジェクトは MIT ライセンスの下でライセンスされています - 詳細は [LICENSE](LICENSE) ファイルを参照してください。

## クレジット

- 原作者：Pengnan Fan
- Python 3.12 互換性のための近代化
