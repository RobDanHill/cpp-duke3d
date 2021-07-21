add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/src/enet)

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

target_include_directories(Engine PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

target_link_libraries(Engine 
  PUBLIC
    enet)
