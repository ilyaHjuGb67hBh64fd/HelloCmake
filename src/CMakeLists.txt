cmake_minimum_required(VERSION 3.2)

if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE "release")
endif()

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall -Werror")
set(CMAKE_CXX_STANDARD_REQUIRED OFF)
#set(CMAKE_CXX_EXTENSIONS OFF)

project(HelloWorld VERSION 1.0.0)

add_library(
	hello
	hello.hpp
	hello.cpp
	)

add_executable(HelloCMkake main.cpp)

target_link_libraries(HelloCMkake PUBLIC hello)

message("CMake " "do " "it " "Look " "whats " "happen)")
