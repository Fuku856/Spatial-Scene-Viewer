# 🎬 3D Spatial Scene Viewer

AI深度推定で生成した3D空間シーンを、カメラ顔追跡で体験できるWebビューアー


**🚀 [Spatial Scene Viewer](https://spatial-scene-viewer.pages.dev)** | **📖 [Spatial Scene Generator](https://huggingface.co/spaces/Ryo563/spatial-scene-generator)**


## ✨ 特徴

- 🎯 **サンプルギャラリー**: 4種類のサンプルですぐに体験可能
- 📁 **ドラッグ&ドロップ**: HTMLファイルを簡単アップロード
- 👁️ **顔追跡**: MediaPipeで高精度な顔認識
- 🎨 **3D視差効果**: 8層のレイヤーによる立体感
- 📱 **レスポンシブ**: PC・スマホ対応
- 🚀 **軽量**: CDNを使用した高速読み込み

## 🎮 使い方

### 1. サンプルで試す
1. [Viewer](https://spatial-scene-viewer.pages.dev)にアクセス
2. サンプルギャラリーから選択
3. 「選択したサンプルを読み込む」をクリック
4. 「3D体験を開始」→「カメラ開始」
5. 顔を動かして3D空間を楽しむ

### 2. 自分の画像で作成
1. [Generator](https://huggingface.co/spaces/Ryo563/spatial-scene-generator)で画像をアップロード
2. 生成されたHTMLファイルをダウンロード
3. Viewerにドラッグ&ドロップ
4. 「3D体験を開始」で体験

## 🛠️ 技術スタック

- **顔検出**: TensorFlow.js + MediaPipe Face Mesh
- **3D表現**: CSS 3D Transforms
- **ホスティング**: Cloudflare Pages
- **UI**: Vanilla JavaScript (ライブラリなし)

## 📂 プロジェクト構成

Spatial-Scene-Viewer/
├── index.html # メインビューアー
├── samples/ # サンプルHTMLファイル
│ ├── ramen.html
│ ├── cat.html
│ ├── person.html
│ └── pagoda.html
└── README.md


## 📝 サンプル追加方法

1. Generatorで画像を処理してHTMLを生成
2. `samples/`フォルダに配置
3. `index.html`の`samples`配列に追加:
{ id: 'new', name: '新サンプル', icon: '🎨', file: '/samples/new.html' }


## 🐛 トラブルシューティング

### カメラが起動しない
- ブラウザのカメラ権限を確認
- HTTPSで接続されているか確認（Cloudflare Pagesは自動HTTPS）

### サンプルが読み込めない
- ブラウザのキャッシュをクリア（Ctrl+Shift+R）
- GitHubのファイルが正しくアップロードされているか確認

### 3D効果が動かない
- 「カメラ開始」ボタンをクリック
- 顔がカメラに映っているか確認
- 明るい場所で試す
- 鼻を隠さない (この顔認識モデルは鼻を使用します)

## 🔗 関連リンク

- **Generator**: [3D Spatial Scene Generator](https://huggingface.co/spaces/Ryo563/spatial-scene-generator)
- **Viewer**: [Viewer](https://spatial-scene-viewer.pages.dev)
- **Hugging Face**: [Hugging Face](https://huggingface.co/spaces/Ryo563/spatial-scene-generator/tree/main)
- **Model**: [Depth-Anything V2](https://huggingface.co/depth-anything/Depth-Anything-V2-Small-hf)

## 🎯 動作原理

1. HTMLファイルに8層のPNG画像（深度別）が埋め込まれている
2. MediaPipeで顔の位置（X, Y, Z）を検出
3. 各レイヤーを顔の動きに応じて移動・回転
4. CSS 3D Transformsで立体感を表現

## 📄 ライセンス

MIT License

## 👨‍💻 開発者

Created by Fuku856

---

**⭐ このプロジェクトが気に入ったら、GitHubでスターをお願いします！**
