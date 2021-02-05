cmake_minimum_required (VERSION 3.11.0)
project(pruebaTest)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED On)
set(CMAKE_CXX_EXTENSIONS Off)
set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} /MTd")

set(CMAKE_INSTALL_PREFIX "../")

add_subdirectory( code  )
add_subdirectory( gtest )