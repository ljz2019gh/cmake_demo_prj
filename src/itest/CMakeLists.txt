project(itest)

add_library(${PROJECT_NAME}
STATIC
test.c
)

set_target_properties(${PROJECT_NAME}
  PROPERTIES
  OUTPUT_NAME "itest"
)

set(CMAKE_LINK_LIBRARY_SUFFIX ".lib")