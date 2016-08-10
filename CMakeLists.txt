project(game.libretro.bsnes-mercury-performance)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(Kodi REQUIRED)
find_package(libretro-bsnes-mercury-performance REQUIRED)

set(DEPLIBS bsnes-mercury-performance)
set(BSNES_MERCURY_CUSTOM_BINARY ${BSNES_MERCURY_LIB}
                                ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX}
                                ${DEPLIBS})

build_addon(${PROJECT_NAME} BSNES_MERCURY DEPLIBS)
