cmake_minimum_required(VERSION 3.0.0)
project(cmakeExperiments VERSION 0.1.0)

#Generate compile_commands.json
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)


#Target
add_executable(main main.cpp src/text.cpp)
#Specify CMake c++23 is necessary
target_compile_features(main PRIVATE cxx_std_23)
#Headers files directory
target_include_directories(main PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)

