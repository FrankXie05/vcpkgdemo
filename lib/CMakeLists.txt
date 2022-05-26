add_library(hello STATIC hello.c)
set_target_properties(hello PROPERTIES OUTPUT_NAME "hello")

install(TARGETS hello
  RUNTIME DESTINATION bin
  LIBRARY DESTINATION lib
  ARCHIVE DESTINATION lib)

install(FILES hello.h DESTINATION "include")
