# masa_interfaces

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![License][license-shield]][license-url]

[JA](README.md) | [EN](README.en.md)

This package contains ROS 2 interface definitions (messages) for the masa project.
It provides standard data structures for 2D object detection.

## Requirements

- OS: Ubuntu (22.04 / 24.04 recommended)
- ROS 2: Humble / Jazzy
- Dependencies: `builtin_interfaces`, `std_msgs`

## Installation

```bash
cd ~/colcon_ws/src
git clone https://github.com/m-shigemori/masa_interfaces.git
cd ~/colcon_ws
colcon build --packages-select masa_interfaces
source install/setup.bash
```

## Usage

The interfaces defined in this package can be used by adding `masa_interfaces` as a dependency in your ROS 2 package's `package.xml` and `CMakeLists.txt`.

### Defined Messages

| Message Name | Description |
|---|---|
| Point2D | Coordinates in 2D space (x, y) |
| KeyPoint2D | Keypoint information for an object (name, score, point) |
| Mask | Contour point array representing an object mask |
| BoundingBox2D | 2D bounding box (center, width, height) |
| ObjectDetection | Single object detection result including class name, score, BBox, keypoints, and mask |
| ObjectDetectionArray | Array of `ObjectDetection` results with a header |

## License

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
