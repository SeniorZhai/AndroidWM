cmake_minimum_required(VERSION 3.4.1)
set(CMAKE_CXX_STANDARD 14)

add_library(
        Watermark
            SHARED
            ${CMAKE_SOURCE_DIR}/Watermark.cpp)

find_library(
              log-lib
              log )

target_link_libraries( # Specifies the target library.
                       Watermark

                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )
