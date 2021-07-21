cmake_minimum_required(VERSION 3.16.2) 

project(cppduke3d VERSION 1.0)

add_subdirectory(Engine)

add_executable(${PROJECT_NAME} ${SOURCES})
target_link_libraries(${PROJECT_NAME} PUBLIC Engine)
