project(cpu)

add_library(${PROJECT_NAME}
  STATIC
  cpu.c
)

set_target_properties(${PROJECT_NAME}
  PROPERTIES
  OUTPUT_NAME "cpu"
)

set(CMAKE_LINK_LIBRARY_SUFFIX ".lib")

