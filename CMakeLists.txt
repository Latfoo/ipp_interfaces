cmake_minimum_required(VERSION 3.5)
project(ipp_interfaces)

find_package(ament_cmake REQUIRED)
find_package(std_msgs REQUIRED)
find_package(geometry_msgs REQUIRED)
find_package(nav_msgs REQUIRED)
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  msg/PolygonsStamped.msg
  srv/SetPath.srv
  DEPENDENCIES std_msgs geometry_msgs nav_msgs
)

ament_package()
