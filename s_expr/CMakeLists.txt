cmake_minimum_required(VERSION 3.5)
project(s_expr)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Threads REQUIRED)
find_package(Boost REQUIRED COMPONENTS system)

include_directories(${Boost_INCLUDE_DIR})
add_executable(s_expr main.cpp)
target_compile_options(s_expr PRIVATE -Wall -pedantic -Werror)
target_link_libraries(s_expr ${CMAKE_THREAD_LIBS_INIT} ${Boost_LIBRARIES})

