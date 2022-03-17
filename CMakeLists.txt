cmake_minimum_required(VERSION 3.22.3)
project(MyProject VERSION 1.0.0 )


add_executable(IMAGEPROCESSING ImageProcessing.cpp)

include_directories(${PROJECT_SOURCE_DIR}/include)
LINK_DIRECTORIES(${PROJECT_SOURCE_DIR}/include)