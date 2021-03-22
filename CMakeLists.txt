cmake_minimum_required(VERSION 3.0.0)
project(sfmltest)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS 1)
set(SFML_DIR ./SFML-2.5.1)

add_subdirectory(./SFML-2.5.1)

find_package(SFML 2.5.1 REQUIRED COMPONENTS graphics window system) # Look for SFML
add_executable(sfmltest main.cpp)
target_link_libraries(sfmltest sfml-graphics sfml-audio sfml-window sfml-system)
