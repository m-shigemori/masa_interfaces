cmake_minimum_required(VERSION 3.8)
project(masa_interfaces)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(builtin_interfaces REQUIRED)
find_package(std_msgs REQUIRED)

set(msg_files
  "msg/Point2D.msg"
  "msg/KeyPoint2D.msg"
  "msg/Mask.msg"
  "msg/BoundingBox2D.msg"
  "msg/ObjectDetection.msg"
  "msg/ObjectDetectionArray.msg"
)

set(srv_files
)

set(action_files
)

set(interface_files
  ${msg_files}
  ${srv_files}
  ${action_files}
)

rosidl_generate_interfaces(${PROJECT_NAME}
  ${interface_files}
  DEPENDENCIES
    builtin_interfaces
    std_msgs
)

ament_package()
