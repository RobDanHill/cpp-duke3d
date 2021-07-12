cmake_minimum_required(VERSION 3.16.2)

add_subdirectory(enet)

target_include_directories(Engine ${CMAKE_CURRENT_SOURCE_DIR}/include)

add_library(Engine STATIC
  ${CMAKE_CURRENT_SOURCE_DIR}/src/cache.c
  ${CMAKE_CURRENT_SOURCE_DIR}/src/display.c
  ${CMAKE_CURRENT_SOURCE_DIR}/src/draw.c
  ${CMAKE_CURRENT_SOURCE_DIR}/src/Engine.c
  ${CMAKE_CURRENT_SOURCE_DIR}/src/filesystem.c
  ${CMAKE_CURRENT_SOURCE_DIR}/src/fixedPoint_math.c
  ${CMAKE_CURRENT_SOURCE_DIR}/src/mmulti.c
  ${CMAKE_CURRENT_SOURCE_DIR}/src/mmulti_stable.cpp
  ${CMAKE_CURRENT_SOURCE_DIR}/src/network.c
  ${CMAKE_CURRENT_SOURCE_DIR}/src/tiles.c)

target_link_libraries(Engine 
  PUBLIC
    enet)
