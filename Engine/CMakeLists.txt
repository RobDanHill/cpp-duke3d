cmake_minimum_required(VERSION 3.16.2)

set(ENGINE_SRC_FILES 
  src/cache.c
  src/display.c
  src/draw.c
  src/Engine.c
  src/filesystem.c
  src/fixedPoint_math.c
  src/mmulti.c
  src/mmulti_stable.cpp
  src/enet/host.c
  src/enet/list.c
  src/enet/memory.c
  src/enet/packet.c
  src/enet/peer.c
  src/enet/protocol.c
  src/enet/unix.c
  src/enet/win32.c
  src/network.c
  src/tiles.c
) 

target_include_directories(Engine src)

add_library(Engine STATIC ${ENGINE_SRC_FILES})
