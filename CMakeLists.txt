project(game.libretro.reicast)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(kodi REQUIRED)
find_package(libretro-reicast REQUIRED)

set(DEPLIBS reicast)
set(REICAST_CUSTOM_BINARY ${REICAST_LIB}
                         ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX} reicast)

build_addon(${PROJECT_NAME} REICAST DEPLIBS)

