cmake_minimum_required(VERSION 3.12)

project(Posix_Threads)

add_executable(my_app main.c)

set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)
target_link_libraries(my_app PRIVATE Threads::Threads)
