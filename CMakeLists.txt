cmake_minimum_required(VERSION 3.22.3)
project(MyProject VERSION 1.0.0 )

#[[
add_executable(IMAGE_Processing ImageProcessing.cpp)

include_directories(${PROJECT_SOURCE_DIR}/include)
LINK_DIRECTORIES(${PROJECT_SOURCE_DIR}/include)
add_library(

)
]]
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES main.cpp)

add_executable(executable ImageProcessing.cpp)
add_definitions( -DMAGICKCORE_QUANTUM_DEPTH=16 )
add_definitions( -DMAGICKCORE_HDRI_ENABLE=0 )
find_package(ImageMagick COMPONENTS Magick++)
include_directories(${ImageMagick_INCLUDE_DIRS})
target_link_libraries(executable ${ImageMagick_LIBRARIES})