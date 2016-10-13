cmake_minimum_required(VERSION 3.1)
project(game.libretro.reicast)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-reicast REQUIRED)

set(DEPLIBS reicast)
set(REICAST_CUSTOM_BINARY ${REICAST_LIB}
                          ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} REICAST DEPLIBS)

