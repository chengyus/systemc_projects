cmake_minimum_required(VERSION 3.10)

project(EventQueueProject)

# Set the SystemC include and library direprocessies
set(SYSTEMC_INCLUDE_DIR $ENV{SYSTEMC_HOME}/include)
set(SYSTEMC_LIBRARY_DIR $ENV{SYSTEMC_HOME}/lib)

# Add the executable
add_executable(event_queue event_queue.cpp)
add_executable(event_queue_dbg event_queue.cpp)

# Link against SystemC
target_include_directories(event_queue PRIVATE ${SYSTEMC_INCLUDE_DIR})
target_link_libraries(event_queue ${SYSTEMC_LIBRARY_DIR}/libsystemc.so)

target_compile_options(event_queue_dbg PRIVATE -g -std=c++17)
target_include_directories(event_queue_dbg PRIVATE ${SYSTEMC_INCLUDE_DIR})
target_link_libraries(event_queue_dbg ${SYSTEMC_LIBRARY_DIR}/libsystemc.so)
