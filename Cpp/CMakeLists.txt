cmake_minimum_required(VERSION 3.20)

project(CNN LANGUAGES CXX)

# Enforce C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Export compile commands for IDEs/tools
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# Binary output directory
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")

# Header include search path
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/inc)

# Collect all .cpp source files from src/
file(GLOB_RECURSE SOURCES CONFIGURE_DEPENDS
    "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp"
)

# Target configuration
if(SOURCES)
    add_executable(cnn_app ${SOURCES})
    target_include_directories(cnn_app PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/inc)
else()
    message(STATUS "No sources found in src/ yet. Add your .cpp files into src/.")
endif()
