cmake_minimum_required(VERSION 3.16)
project(vaudio_minimp3)

set(SRCDIR "${CMAKE_CURRENT_SOURCE_DIR}/../../..")
set(CMAKE_MODULE_PATH "${SRCDIR}/cmake")

include(source_dll_base)


## Source Files ##

target_sources(${PROJECT_NAME} PRIVATE "vaudio_minimp3.cpp")


## Header Files ##

file(GLOB SRC_HEADER_FILES "*.h")
target_sources(${PROJECT_NAME} PRIVATE ${SRC_HEADER_FILES})


## Link Libraries ##

# System libs must be linked last!
target_link_libraries(${PROJECT_NAME} ${SYSTEM_LIBS})
