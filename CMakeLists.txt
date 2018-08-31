cmake_minimum_required(VERSION 3.1)
project(game.libretro.mame2003-plus)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-mame2003-plus REQUIRED)

set(MAME2003PLUS_CUSTOM_BINARY ${MAME2003PLUS_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} MAME2003PLUS "")
