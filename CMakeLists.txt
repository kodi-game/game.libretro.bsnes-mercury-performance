cmake_minimum_required(VERSION 3.1)
project(game.libretro.bsnes-mercury-performance)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-bsnes-mercury-performance REQUIRED)

set(BSNES-MERCURY-PERFORMANCE_CUSTOM_BINARY ${BSNES-MERCURY-PERFORMANCE_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BSNES-MERCURY-PERFORMANCE "")

include(CPack)
