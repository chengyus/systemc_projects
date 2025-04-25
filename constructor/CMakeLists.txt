cmake_minimum_required(VERSION 3.5)

project(ConstructorProject)

# Set the SystemC include and library directories
set(SYSTEMC_INCLUDE_DIR $ENV{SYSTEMC_HOME}/include)
set(SYSTEMC_LIBRARY_DIR $ENV{SYSTEMC_HOME}/lib)

# Add the executable
add_executable(ctor ctor.cpp)

# Link against SystemC
target_include_directories(ctor PRIVATE ${SYSTEMC_INCLUDE_DIR})
target_link_libraries(ctor ${SYSTEMC_LIBRARY_DIR}/libsystemc.so)
