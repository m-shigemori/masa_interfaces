# masa_interfaces

[JA](README.md) | [EN](README.en.md)

This package contains ROS 2 interface definitions (messages) for the masa project.
It provides standard data structures for 2D object detection.

## Requirements

- OS: Ubuntu
- ROS 2 (Humble/Iron/Jazzy/Rolling)
- builtin_interfaces
- std_msgs

## Installation

1. Navigate to the `src` directory of your ROS 2 workspace.
```bash
cd ~/colcon_ws/src
```
2. Clone this repository (replace with the actual URL).
```bash
git clone <repository_url>
```
3. Navigate to the workspace root and build the package.
```bash
cd ~/colcon_ws
colcon build --packages-select masa_interfaces
```
4. Source the workspace.
```bash
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

Apache-2.0
