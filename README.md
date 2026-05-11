# masa_interfaces

[JA](README.md) | [EN](README.en.md)

masaプロジェクトのためのROS 2インターフェース定義（メッセージ）パッケージです。
2D物体検出に関連する標準的なデータ構造を提供します。

## 必要条件

- OS: Ubuntu
- ROS 2 (Humble/Iron/Jazzy/Rolling)
- builtin_interfaces
- std_msgs

## インストール

1. ROS 2ワークスペースの `src` ディレクトリに移動します。
```bash
cd ~/colcon_ws/src
```
2. このリポジトリをクローンします（実際のURLに置き換えてください）。
```bash
git clone <repository_url>
```
3. ワークスペースのルートに移動し、ビルドします。
```bash
cd ~/colcon_ws
colcon build --packages-select masa_interfaces
```
4. ワークスペースをソースします。
```bash
source install/setup.bash
```

## 使用方法

他のROS 2パッケージの `package.xml` および `CMakeLists.txt` に `masa_interfaces` を依存関係として追加することで、定義されたメッセージを利用できます。

### 定義されているメッセージ

| メッセージ名 | 説明 |
|---|---|
| Point2D | 2D空間上の座標 (x, y) |
| KeyPoint2D | 物体の特定部位を示すキーポイント (名前, スコア, 座標) |
| Mask | 物体の領域を示すマスク情報の輪郭点配列 |
| BoundingBox2D | 2Dバウンディングボックス (中心座標, 幅, 高さ) |
| ObjectDetection | クラス名、信頼度スコア、および上記のBBox、キーポイント、マスクを含む単一の物体検出結果 |
| ObjectDetectionArray | 検出された複数の物体を格納する `ObjectDetection` の配列（Header付き） |

## ライセンス

Apache-2.0
