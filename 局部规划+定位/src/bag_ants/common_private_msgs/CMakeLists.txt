cmake_minimum_required(VERSION 3.0.2)
project(common_private_msgs)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  std_msgs
  geometry_msgs
  message_generation
)

add_message_files(
  FILES
  Node.msg
  Graph.msg
  vehicle_param.msg
  vehicle_status.msg
  planning_info.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime
)