cmake_minimum_required(VERSION 3.24)

project(my_service LANGUAGES CXX)

find_package(userver REQUIRED COMPONENTS core)

add_executable(my_service src/main.cpp)

target_compile_features(my_service PRIVATE cxx_std_20)

target_link_libraries(my_service PRIVATE userver::core)