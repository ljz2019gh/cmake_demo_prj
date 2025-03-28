project(demo_src)

add_subdirectory(cpu)
add_subdirectory(itest)
add_subdirectory(cstart)

# Set output suffix and path
set(CMAKE_EXECUTABLE_SUFFIX .elf)
add_executable(demo main.c
  ${cpu_dir}/cpu.c
  ${itest_dir}/test.c
  ${cstart_dir}/cstart.c)


set_target_properties(demo PROPERTIES OUTPUT_NAME "demo")
