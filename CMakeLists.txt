cmake_minimum_required(VERSION 4.3)
project(learning)

set(CMAKE_CXX_STANDARD 20)

add_executable(learning main.cpp)

add_custom_target(run
    COMMAND ${CMAKE_COMMAND} -E echo
    COMMAND learning
    DEPENDS learning
    WORKING_DIRECTORY ${CMAKE_SOURCE_DIR}
    COMMENT "Running learning"
    USES_TERMINAL
    VERBATIM
)
