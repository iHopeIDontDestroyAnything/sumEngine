cmake_minimum_required(VERSION 3.15)
project(jajo
  VERSION 1.0
  LANGUAGES CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_subdirectory(${CMAKE_SOURCE_DIR}/JajoEngine)
add_subdirectory(${CMAKE_SOURCE_DIR}/sandbox)



