add_library(enet STATIC
  host.c
  list.c
  memory.c
  packet.c
  peer.c
  protocol.c
  unix.c
  win32.c)
target_include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)
