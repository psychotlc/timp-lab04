cmake_minimum_required(VERSION 3.4)

include_directories(formatter_lib formatter_ex_lib solver_lib)
add_subdirectory(formatter_lib)
add_subdirectory(formatter_ex_lib)
add_subdirectory(solver_lib)

add_executable(hello_world hello_world_application/hello_world.cpp )
target_link_libraries(hello_world formatter_ex)

add_executable(equation solver_application/equation.cpp)
target_link_libraries(equation solver formatter_ex)