# masa_interfaces

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![License][license-shield]][license-url]

[JA](README.md) | [EN](README.en.md)

masaプロジェクトのためのROS 2インターフェース定義（メッセージ）パッケージです。
2D物体検出に関連する標準的なデータ構造を提供します。

## 必要条件

- OS: Ubuntu (22.04 / 24.04推奨)
- ROS 2: Humble / Jazzy
- 依存パッケージ: `builtin_interfaces`, `std_msgs`

## インストール

```bash
cd ~/colcon_ws/src
git clone https://github.com/m-shigemori/masa_interfaces.git
cd ~/colcon_ws
colcon build --packages-select masa_interfaces
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

[BSD 3-Clause License](LICENSE)

[contributors-shield]: https://img.shields.io/github/contributors/m-shigemori/masa_interfaces?style=for-the-badge
[contributors-url]: https://github.com/m-shigemori/masa_interfaces/graphs/contributors

[forks-shield]: https://img.shields.io/github/forks/m-shigemori/masa_interfaces?style=for-the-badge
[forks-url]: https://github.com/m-shigemori/masa_interfaces/network/members

[stars-shield]: https://img.shields.io/github/stars/m-shigemori/masa_interfaces?style=for-the-badge
[stars-url]: https://github.com/m-shigemori/masa_interfaces/stargazers

[issues-shield]: https://img.shields.io/github/issues/m-shigemori/masa_interfaces?style=for-the-badge
[issues-url]: https://github.com/m-shigemori/masa_interfaces/issues

[license-shield]: https://img.shields.io/github/license/m-shigemori/masa_interfaces?style=for-the-badge
[license-url]: https://github.com/m-shigemori/masa_interfaces/blob/main/LICENSE
