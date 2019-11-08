cmake_minimum_required(VERSION 3.1)
project(
  stb
  VERSION 0.1
  LANGUAGES C CXX)

set(STB_SOURCE_DIR "${CMAKE_CURRENT_SOURCE_DIR}")

add_library(stb "${STB_SOURCE_DIR}/stb_image.c"
                "${STB_SOURCE_DIR}/stb_image_write.c")
target_include_directories(stb PUBLIC "${STB_SOURCE_DIR}")

add_library(stb::stb ALIAS stb)
