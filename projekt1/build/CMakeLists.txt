cmake_minimum_required(VERSION 3.20)
project(projekt1)
include_directories(../inc)
add_executable(run_projekt1 ../src/main.c ../src/gpiod_utils.c ../src/semaphore.c)
target_compile_options(run_projekt1 PRIVATE -Wall -Werror)
target_link_libraries(run_projekt1 gpiod pthread)
set_target_properties(run_projekt1 PROPERTIES RUNTIME_OUTPUT_DIRECTORY ../)

