cmake_minimum_required(VERSION 3.10)

set(CMAKE_CXX_STANDARD 17)

#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}) #-pthread")

find_package(Threads)

include_directories(./bin/include ./bin/common)
link_directories(./bin/linux-gcc-64)

add_executable(exe	main.cpp)
target_link_libraries(exe	libIrrKlang.so)
target_link_libraries(exe	${CMAKE_THREAD_LIBS_INIT})
