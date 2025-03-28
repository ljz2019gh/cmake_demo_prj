project(cstart)

add_library(${PROJECT_NAME}
STATIC
cstart.c
)

set_target_properties(${PROJECT_NAME}
  PROPERTIES
  OUTPUT_NAME "cstart"
)

set(CMAKE_LINK_LIBRARY_SUFFIX ".lib")