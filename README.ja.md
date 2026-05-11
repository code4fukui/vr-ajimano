# vr-ajimano

フォトグラメトリを活用して作成された、味真野小学校の桜を体験できるVRおよび3Dマッププロジェクトです。

## デモ

- **[マップ上の3Dモデル](https://code4fukui.github.io/vr-ajimano/map.html)**: 実際の地理的位置に学校の3Dモデルを表示するインタラクティブなマップ。
- **[VRグラウンドビュー](https://code4fukui.github.io/vr-ajimano/ground.html)**: 地上視点から桜を体験できる没入型VRツアー。
- **[VR空間の6本の桜](https://code4fukui.github.io/vr-ajimano/sakuras.html)**: 6本の桜の木のモデルが円形に配置されたバーチャル空間。

## プロジェクト概要

本プロジェクトは、味真野小学校の桜の風景をデジタルで保存・共有するものです。フォトグラメトリでスキャンした3Dモデルと、WebVR（A-Frame）および3Dマップ（MapLibre GL JS）を組み合わせ、ブラウザから直接アクセスできる没入型体験を提供します。

## 特徴

- **3Dマップの統合**: MapLibre GL JSとカスタムレイヤー（`getModelLayer.js`）を使用し、`.glb`モデルを3Dマップ上にレンダリングします。
- **没入型VRシーン**: A-Frameで構築されており、テレポート機能と一人称視点のカメラコントロール（`mc-controls.js`）を備えています。
- **フォトグラメトリモデル**: 2つの詳細なGLBモデルが含まれています。`ajimano-sakura-ground.glb`（周囲の地面を含む木）と`ajimano-sakura.glb`（単体の木）。
- **クロスプラットフォーム**: デスクトップブラウザで動作し、WebXRをサポートするVRヘッドセットにも対応しています。

## はじめに

このプロジェクトをローカルで実行するには、ローカルWebサーバーが必要です。

1. リポジトリをクローンします:
    ```sh
    git clone https://github.com/code4fukui/vr-ajimano.git
    ```
2. プロジェクトディレクトリに移動します:
    ```sh
    cd vr-ajimano
    ```
3. ローカルWebサーバーを起動します（例: Pythonを使用）:
    ```sh
    python -m http.server
    ```
4. Webブラウザを開き、HTMLファイル（例: `http://localhost:8000/map.html`）にアクセスします。

## 主なコンポーネント

- **3Dモデル**:
  - `ajimano-sakura-ground.glb`: 地面を含むメインモデル。`map.html`および`ground.html`で使用されます。
  - `ajimano-sakura.glb`: 単体の桜の木のモデル。`sakuras.html`で使用されます。
- **コアスクリプト**:
  - `getModelLayer.js`: MapLibre GL JS用のカスタム3Dモデルレイヤーを作成するモジュール。
  - `mc-controls.js`: A-Frameシーン向けにMinecraft風の一人称視点コントロールを提供します。
- **マップスタイル**:
  - マップビューでは、デフォルトの3D建物を非表示にするために[カスタムMapLibreスタイルJSON](https://code4fukui.github.io/vrmap/mapsetting_nobuilding.json)を使用しています。

## 依存関係

本プロジェクトは、CDN経由で読み込まれる以下の外部ライブラリに依存しています:

- [A-Frame](https://aframe.io/)
- [Three.js](https://threejs.org/)
- [MapLibre GL JS](https://maplibre.org/)

## ライセンス

CC BY Open Data by Code for FUKUI / [デジタルツイン越前製作実行委員会](https://code4fukui.github.io/digitaltwin/)
