add_library(hello_static STATIC hello.c)
set_target_properties(hello_static PROPERTIES OUTPUT_NAME "hello")
target_include_directories(hello_static PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}> $<INSTALL_INTERFACE:include>)

install (TARGETS hello_static
  EXPORT unofficial-hello_static-config
  RUNTIME DESTINATION bin
  LIBRARY DESTINATION lib
  ARCHIVE DESTINATION lib)

install(EXPORT unofficial-hello_static-config DESTINATION share/unofficial-hello_static-config)
install (FILES hello.h DESTINATION "include")
