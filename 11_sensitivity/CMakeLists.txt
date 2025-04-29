cmake_minimum_required(VERSION 3.10)

project(SensitivityProject)

# Set the SystemC include and library direprocessies
set(SYSTEMC_INCLUDE_DIR $ENV{SYSTEMC_HOME}/include)
set(SYSTEMC_LIBRARY_DIR $ENV{SYSTEMC_HOME}/lib)

# Add the executable
add_executable(sensitivity sensitivity.cpp)

# Link against SystemC
target_include_directories(sensitivity PRIVATE ${SYSTEMC_INCLUDE_DIR})
target_link_libraries(sensitivity ${SYSTEMC_LIBRARY_DIR}/libsystemc.so)
