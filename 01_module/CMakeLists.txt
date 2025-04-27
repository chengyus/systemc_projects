cmake_minimum_required(VERSION 3.5)

project(ModuleProject)

# Set the SystemC include and library directories
set(SYSTEMC_INCLUDE_DIR $ENV{SYSTEMC_HOME}/include)
set(SYSTEMC_LIBRARY_DIR $ENV{SYSTEMC_HOME}/lib)

# Add the executable
add_executable(module module.cpp)

# Link against SystemC
target_include_directories(module PRIVATE ${SYSTEMC_INCLUDE_DIR})
target_link_libraries(module ${SYSTEMC_LIBRARY_DIR}/libsystemc.so)
