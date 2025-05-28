cmake_minimum_required(VERSION 3.15)
project(sandbox
  VERSION 1.0
  LANGUAGES CXX)

set(JajoEngine ${CMAKE_SOURCE_DIR}/bin/libJajo.so)

include_directories(${CMAKE_SOURCE_DIR}/include)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR})

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(CPP_SOURCES
  src/main.cpp)

add_executable(run ${CPP_SOURCES})

set_target_properties(run PROPERTIES
                    CMAKE_BUILD_WITH_INSTALL_RPATH FALSE
                    LINK_FLAGS "-Wl,-rpath,$ORIGIN/")

target_link_libraries(run ${JajoEngine})
