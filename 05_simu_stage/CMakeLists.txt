cmake_minimum_required(VERSION 3.10)

project(SimulationStagesProject)

# Set the SystemC include and library direprocessies
set(SYSTEMC_INCLUDE_DIR $ENV{SYSTEMC_HOME}/include)
set(SYSTEMC_LIBRARY_DIR $ENV{SYSTEMC_HOME}/lib)

# Add the executable
add_executable(simu_stage simu_stage.cpp)

# Link against SystemC
target_include_directories(simu_stage PRIVATE ${SYSTEMC_INCLUDE_DIR})
target_link_libraries(simu_stage ${SYSTEMC_LIBRARY_DIR}/libsystemc.so)
