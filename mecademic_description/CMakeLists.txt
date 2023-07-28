cmake_minimum_required(VERSION 3.15)
project(mecademic_description)

# default to C99
if(NOT CMAKE_C_STANDARD)
  set(CMAKE_C_STANDARD 99)
endif ()

# default to C++17
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 17)
endif ()

if(CMAKE_COMPILER_IS_GNUXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_definitions(-Wall -Wextra -Wpedantic)
endif()

find_package(ament_cmake_auto REQUIRED)

install(DIRECTORY meshes ros2_control urdf DESTINATION share/${PROJECT_NAME})

ament_auto_package()
