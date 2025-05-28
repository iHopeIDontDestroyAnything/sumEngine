cmake_minimum_required(VERSION 3.15)
project(Jajo
  VERSION 1.0
  LANGUAGES CXX)

set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)


set(CPP_SOURCES
  src/Jajo.cpp
  )

set(H_SOURCES
  include/Jajo.h
  )

add_library(${PROJECT_NAME} SHARED ${CPP_SOURCES})
target_include_directories(${PROJECT_NAME} PUBLIC include)

file(COPY include
     DESTINATION ${CMAKE_SOURCE_DIR})
