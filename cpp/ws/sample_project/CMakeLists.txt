cmake_minimum_required(VERSION 2.6)
project(sample)

# add_library(greeting STATIC
#   lib/hello.cpp
# )

add_library(greeting SHARED
  lib/hello.cpp
)

include_directories(
  lib
)

add_executable(sample1
  src/sample1/sample1.cpp
)

target_link_libraries(sample1
  greeting
)
