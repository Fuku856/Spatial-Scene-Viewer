## 📌 3D Spatial Scene Viewer - # Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## 今後の予定

### v1.1.0（正式版）予定
- v1.1.0-betaの動作検証完了後にリリース
- 背景画像の最適化（WebP変換など）
- モバイル最適化
- クロスブラウザテスト完了
- UI非表示機能の追加

### v1.2.0 検討中
- ジャイロスコープ対応（モバイル）
- エフェクト追加（パーティクル、グロー）
- テーマ追加（3種類目以降）
- ソーシャルシェア機能

---

## [v1.1.0-beta] - 2025-10-13
https://github.com/Fuku856/Spatial-Scene-Viewer/releases/tag/v1.1.0-beta

**⚠️ ベータ版リリース**（動作未検証・実験的機能）

### Added
- 🎨 **背景テーマ切り替え機能**（実験的）
  - 🌈 グラデーションテーマ（デフォルト）
  - ⭐ 星空テーマ（2枚の宇宙背景画像 + 150個の動くCSS星）
- 💾 **テーマ設定の永続化**
  - localStorageを使用したテーマの記憶機能
  - 次回訪問時も選択したテーマを自動適用
- 🌟 **星空エフェクト**
  - 背景画像の360度ゆっくり回転アニメーション
  - CSS星の浮遊・点滅アニメーション（1-3pxのランダムサイズ）
  - グラデーション背景のシフトアニメーション
- 🎛️ **テーマ切り替えボタン**
  - 右下に配置（PC/モバイル対応）
  - ワンクリックでテーマ変更

### Changed
- 🎨 **ビューアーUI改善**
  - カメラプレビューを左下から右下に移動（140×105px）
  - トラッキングステータスを下中央から上中央に移動
  - タイトルバーを2段構成に変更（タイトル行 + コントロール行）
- 🎯 **ボタンの視認性向上**
  - カメラ開始ボタン: 緑（success）
  - カメラ停止ボタン: オレンジ（warning）
  - 閉じるボタン: 赤（danger）
  - 各ボタンにアイコンを追加
- 📐 **レイアウト最適化**
  - UI要素の重なり問題を解消
  - シーンコンテナの開始位置を調整（top: 60px → 90px）
  - モバイル表示の改善

### Fixed
- 🐛 カメラプレビューとステータス表示の重なり問題を修正
- 🐛 モバイルでのボタン配置を改善

### Known Issues
- 背景画像の読み込み速度が未検証（ファイルサイズ: skystarfield 1.2MB / cosmostar 675KB）
- モバイル環境でのアニメーションパフォーマンス未確認
- 一部ブラウザでのCSS回転アニメーション互換性未テスト
- Safari/iOSでのbackdrop-filter動作未検証


### Required Assets
assets/
├── skystarfield_aom_lq.jpg (1.2MB)
└── cosmostar_aom_lq.jpg (675KB)


---

## [v1.0.0] - 2025-10-12
https://github.com/Fuku856/Spatial-Scene-Viewer/releases/tag/v1.0.0

**🎉 初回リリース**

### Added
- 📁 **HTMLファイルアップロード機能**
  - ドラッグ&ドロップ対応
  - ファイル検証機能（spatial-scene-generatorメタタグチェック）
- 🎯 **サンプルギャラリー**
  - 4種類のサンプルシーン（ラーメン、ネコ、人物、五重塔）
  - ワンクリックでサンプル読み込み
- 👁️ **MediaPipe顔追跡**
  - TensorFlow.js + MediaPipe Face Mesh
  - リアルタイム顔位置検出（X/Y/Z軸）
- 🎬 **8層レイヤー3D視差効果**
  - CSS 3D Transforms
  - スムーズな視差移動
  - 深度に応じた回転・スケール
- 📹 **カメラプレビュー**
  - 左下にカメラ映像表示
  - トラッキングステータス表示
- 🔄 **カメラリセット機能**
  - ワンクリックで初期位置に復帰
- ⌨️ **キーボードショートカット**
  - ESCキーでビューアーを閉じる
  
