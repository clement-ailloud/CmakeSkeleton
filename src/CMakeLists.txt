cmake_minimum_required (VERSION 2.6)

###############################################################################
#
# 	Executable
#
###############################################################################

add_executable (${PROJECT_NAME} "main.cpp")

###############################################################################
#
# 	Target Link Libraries
#
###############################################################################

target_link_libraries (${PROJECT_NAME} HelloWorldLibrary)

###############################################################################
#
# 	Target properties
#
###############################################################################

set_target_properties(${PROJECT_NAME}
	PROPERTIES OUTPUT_NAME "helloworld")

###############################################################################
#
# 	Install
#
###############################################################################

install (TARGETS ${PROJECT_NAME} DESTINATION "$ENV{HOME}/bin")
