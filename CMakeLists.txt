cmake_minimum_required(VERSION 3.25)

project(svr07 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include(generated/rexglue.cmake)

set(SVR07_SOURCES
  src/main.cpp
)

if(WIN32)
  add_executable(svr07 WIN32 ${SVR07_SOURCES})
else()
  add_executable(svr07 ${SVR07_SOURCES})
endif()

rexglue_setup_target(svr07)