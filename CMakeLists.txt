cmake_minimum_required(VERSION 3.20)
project(EmptyWindowCpp LANGUAGES CXX)

add_executable(EmptyWindow WIN32 src/main.cpp)
target_compile_features(EmptyWindow PRIVATE cxx_std_17)
target_compile_definitions(EmptyWindow PRIVATE UNICODE _UNICODE)
