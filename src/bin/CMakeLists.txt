add_library(hello_shared SHARED dll.cpp)
set_target_properties(hello_shared PROPERTIES OUTPUT_NAME "hello_dll")


install (TARGETS hello_shared
  RUNTIME DESTINATION bin
  LIBRARY DESTINATION lib
  ARCHIVE DESTINATION lib)

install (FILES dll.h DESTINATION "include")