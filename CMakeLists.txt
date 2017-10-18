project(testGmockProject)
cmake_minimum_required(VERSION 3.0)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")

set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)

set(sources 
   main.cpp 
   TestMock.cpp)
add_executable(testGmockProject ${sources})

target_link_libraries(testGmockProject Threads::Threads)
target_link_libraries(testGmockProject gmock)
target_link_libraries(testGmockProject gtest)

