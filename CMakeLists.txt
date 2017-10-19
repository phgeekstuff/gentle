#
# CMake File to build gentle.
#

cmake_minimum_required (VERSION 2.6)
project (gentle)

# version number
set (GENTLE_VERSION_MAJOR 0)
set (GENTLE_VERSION_MINOR 1)
set (GENTLE_VERSION_BUILD 1)
set (GENTLE_VERSION_BUILD 1)

# adding and including folders

include_directories ("${PROJECT_INCLUDE_DIR}")
 
# configure a header file to pass some of the CMake settings
# to the source code
configure_file (
  "${PROJECT_SOURCE_DIR}/TutorialConfig.h.in"
  "${PROJECT_BINARY_DIR}/TutorialConfig.h"
  )
 
# add the binary tree to the search path for include files
# so that we will find TutorialConfig.h
include_directories("${PROJECT_BINARY_DIR}")
 
# add the executable
add_executable(gentle "${PROJECT_SOURCE_DIR}/TutorialConfig.h.in")