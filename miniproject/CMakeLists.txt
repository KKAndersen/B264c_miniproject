cmake_minimum_required(VERSION 2.8.3)
project(agitr)

find_package(catkin REQUIRED COMPONENTS 
	roscpp
	geometry_msgs 
	turtlesim
	std_msgs
	)

catkin_package( CATKIN_DEPENDS 
	roscpp 
	std_msgs
	geometry_msgs 
	turtlesim 
)

add_executable(spawn src/spawn.cpp)
add_executable(approach src/approach.cpp)

target_link_libraries(approach ${catkin_LIBRARIES})
target_link_libraries(spawn ${catkin_LIBRARIES})

