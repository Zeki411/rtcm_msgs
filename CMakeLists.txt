cmake_minimum_required(VERSION 3.5)
project(rtcm_msgs)


find_package(std_msgs REQUIRED)

find_package(ament_cmake REQUIRED)
find_package(builtin_interfaces REQUIRED)
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME} ADD_LINTER_TESTS
  msg/Message.msg
  DEPENDENCIES builtin_interfaces std_msgs
)
ament_export_dependencies(rosidl_default_runtime)
ament_package()

