cmake_minimum_required (VERSION 2.6)

set (PROJECT_NAME "HelloCMake")

project (${PROJECT_NAME})

set (${PROJECT_NAME}_VERSION_MAJOR 1)
set (${PROJECT_NAME}_VERSION_MINOR 0)

###############################################################################
#
# 	Cmake package module
#
###############################################################################

#include (InstallRequiredSystemLibraries)

#set (CPACK_RESOURCE_FILE_LICENSE ${CMAKE_CURRENT_SOURCE_DIR}/License.txt)
#set (CPACK_PACKAGE_VERSION_MAJOR ${${PROJECT_NAME}_VERSION_MAJOR})
#set (CPACK_PACKAGE_VERSION_MINOR ${${PROJECT_NAME}_VERSION_MINOR})

#include (CPack)

###############################################################################
#
# 	Subdirectories
#
###############################################################################

add_subdirectory ("src")

###############################################################################
#
# 	Subdirectories
#
###############################################################################

add_subdirectory ("lib/hello_world-1.0")

###############################################################################
#
# 	Target properties
#
###############################################################################

set_target_properties (${PROJECT_NAME} 
	PROPERTIES RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")
