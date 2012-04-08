cmake_minimum_required (VERSION 2.6) 
project (snakecore) 

add_subdirectory(lib)
add_subdirectory("include")

find_package (Threads)

include_directories ("${PROJECT_SOURCE_DIR}/include")
add_library(snakecore ${SNAKE_CORE_HEADERS} ${SNAKE_CORE_SOURCES})
target_link_libraries(snakecore ${CMAKE_THREAD_LIBS_INIT})




