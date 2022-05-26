
include_directories(${CMAKE_SOURCE_DIR}/lib)
include_directories(${CMAKE_SOURCE_DIR}/src/bin)
add_executable(main "bin/dll.cpp")
target_link_libraries(main hello_shared)
