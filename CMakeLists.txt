cmake_minimum_required(VERSION 2.8.3)
project(tiny_msgs)

find_package(catkin REQUIRED COMPONENTS 
	std_msgs 
	message_generation
)

add_message_files(
  FILES
  tinyVector.msg
  tinyIMU.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)
