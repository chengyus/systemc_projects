cmake_minimum_required(VERSION 3.10)

project(CombinedEventsProject)

# Set the SystemC include and library direprocessies
set(SYSTEMC_INCLUDE_DIR $ENV{SYSTEMC_HOME}/include)
set(SYSTEMC_LIBRARY_DIR $ENV{SYSTEMC_HOME}/lib)

# Add the executable
add_executable(combined_events event_combined.cpp)

# Link against SystemC
target_include_directories(combined_events PRIVATE ${SYSTEMC_INCLUDE_DIR})
target_link_libraries(combined_events ${SYSTEMC_LIBRARY_DIR}/libsystemc.so)
