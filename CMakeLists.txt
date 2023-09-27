cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_STANDARD 14)
project(Visual_Trilateration)

find_package(OpenCV REQUIRED)
include_directories(${TensorFlowLite_INCLUDE_DIRS} ${OpenCV_INCLUDE_DIRS})
ADD_LIBRARY(tensorflowlite SHARED IMPORTED)


add_executable(Visual_Trilateration Visual_Trilateration.cpp)
target_link_libraries(Visual_Trilateration ${TensorFlowLite_LIBS} ${OpenCV_LIBS})
