cmake_minimum_required(VERSION 2.8.9)

set(TARGET_NAME myProgram)
project(${TARGET_NAME})

#Bring the headers, such as Student.h into the project
include_directories(include)
include_directories(".")

file(GLOB INCLUDES "include/*.h")
#However, the file(GLOB...) allows for wildcard additions:
file(GLOB SOURCES "src/*.cpp")

add_library(add ${SOURCES} ${INCLUDES})

add_executable(${TARGET_NAME} ${SOURCES} ${INCLUDES})

target_link_libraries(${TARGET_NAME} add)

install(TARGETS ${TARGET_NAME} DESTINATION deploy)