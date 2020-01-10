cmake_minimum_required(VERSION 3.10)

project(lab3)

enable_testing()

set(Figures_source Figures.cpp)

add_library(figures STATIC ${Figures_source})

find_package(Boost COMPONENTS unit_test_framework REQUIRED)



add_executable(lab3
main.cpp
Figures.cpp)

set_property(TARGET lab3 PROPERTY CXX_STANDARD 17)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Werror")
