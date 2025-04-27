cmake_minimum_required(VERSION 3.5)

project(SimulationProcessProject)

# Set the SystemC include and library direprocessies
set(SYSTEMC_INCLUDE_DIR $ENV{SYSTEMC_HOME}/include)
set(SYSTEMC_LIBRARY_DIR $ENV{SYSTEMC_HOME}/lib)

# Add the executable
add_executable(simu_proc simu_process.cpp)

# Link against SystemC
target_include_directories(simu_proc PRIVATE ${SYSTEMC_INCLUDE_DIR})
target_link_libraries(simu_proc ${SYSTEMC_LIBRARY_DIR}/libsystemc.so)
