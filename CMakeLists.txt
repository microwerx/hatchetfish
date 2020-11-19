cmake_minimum_required(VERSION 3.16)
project(hatchetfish)

set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_STANDARD 17)

if (APPLE)
   include_directories(/usr/local/include)
   link_directories(/usr/local/lib)
endif()

include_directories(${PROJECT_SOURCE_DIR}/include)

add_library(${PROJECT_NAME} STATIC
    src/hatchetfish_log.cpp
    src/hatchetfish_stopwatch.cpp
    )
