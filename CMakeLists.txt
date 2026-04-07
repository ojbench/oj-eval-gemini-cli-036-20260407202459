cmake_minimum_required(VERSION 3.10)
project(dynamic_bitset)

set(CMAKE_CXX_STANDARD 17)

file(GLOB SOURCES "*.cpp")

if(SOURCES)
    add_executable(code ${SOURCES})
else()
    # If no cpp files, create a dummy one to satisfy the requirement of building 'code'
    file(WRITE dummy.cpp "int main() { return 0; }")
    add_executable(code dummy.cpp)
endif()
