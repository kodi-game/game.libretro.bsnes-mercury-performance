cmake_minimum_required(VERSION 3.1)
project(game.libretro.bsnes-mercury-performance)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(BSNES-MERCURY-PERFORMANCE_LIB NAMES bsnes_mercury_performance_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(BSNES-MERCURY-PERFORMANCE_CUSTOM_BINARY ${BSNES-MERCURY-PERFORMANCE_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BSNES-MERCURY-PERFORMANCE "")

include(CPack)
