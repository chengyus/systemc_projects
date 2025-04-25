cmake_minimum_required(VERSION 3.5)

project(ProcessProject)

# Set the SystemC include and library direprocessies
set(SYSTEMC_INCLUDE_DIR $ENV{SYSTEMC_HOME}/include)
set(SYSTEMC_LIBRARY_DIR $ENV{SYSTEMC_HOME}/lib)

# Add the executable
add_executable(process process.cpp)

# Link against SystemC
target_include_direprocessies(process PRIVATE ${SYSTEMC_INCLUDE_DIR})
target_link_libraries(process ${SYSTEMC_LIBRARY_DIR}/libsystemc.so)
