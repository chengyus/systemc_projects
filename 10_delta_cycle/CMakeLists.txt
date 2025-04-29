cmake_minimum_required(VERSION 3.10)

project(DeltaCycleProject)

# Set the SystemC include and library direprocessies
set(SYSTEMC_INCLUDE_DIR $ENV{SYSTEMC_HOME}/include)
set(SYSTEMC_LIBRARY_DIR $ENV{SYSTEMC_HOME}/lib)

# Add the executable
add_executable(delta_cycle delta_cycle.cpp)

# Link against SystemC
target_include_directories(delta_cycle PRIVATE ${SYSTEMC_INCLUDE_DIR})
target_link_libraries(delta_cycle ${SYSTEMC_LIBRARY_DIR}/libsystemc.so)
