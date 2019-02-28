cmake_minimum_required (VERSION 2.6)

set (PROJECT_NAME "HelloWorldLibrary")

project (${PROJECT_NAME})

set (${PROJECT_NAME}_VERSION_MAJOR 1)
set (${PROJECT_NAME}_VERSION_MINOR 0)

add_library (${PROJECT_NAME} "src/hello_world.cpp")

target_include_directories (${PROJECT_NAME} PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include")

set_target_properties (${PROJECT_NAME}
	PROPERTIES LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")

#install (FILES )
