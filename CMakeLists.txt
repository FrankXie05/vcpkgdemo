cmake_minimum_required(VERSION 3.8)

project(vcpkgdemo)


add_subdirectory(lib)
add_subdirectory(src bin)

include (CPack)
