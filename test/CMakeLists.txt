cmake_minimum_required(VERSION 3.8)

project(test)

add_subdirectory(lib/googletest)

include_directories(lib/googletest/googletest/include)

set(SOURCE main.cpp )

add_executable(test ${SOURCE})
target_link_libraries(test gtest)
install(TARGETS test DESTINATION build)