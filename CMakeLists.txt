cmake_minimum_required(VERSION 3.15)
project(PR_Lab2)

find_package(MPI)
include_directories(${MPI_INCLUDE_PATH})

set(CMAKE_CXX_STANDARD 11)

add_executable(PR_Lab2 mysort.c)

target_compile_options(PR_Lab2 PRIVATE ${MPI_CXX_COMPILE_FLAGS})
target_link_libraries(PR_Lab2 ${MPI_CXX_LIBRARIES} ${MPI_CXX_LINK_FLAGS})