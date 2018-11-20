cmake_minimum_required(VERSION 3.1)
project(game.libretro.beetle-wswan)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(BEETLE-WSWAN_LIB NAMES mednafen_wswan_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(BEETLE-WSWAN_CUSTOM_BINARY ${BEETLE-WSWAN_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BEETLE-WSWAN "")

include(CPack)
