cmake_minimum_required (VERSION 3.10)

################
# Project
################ 
project (opengl_test)

################
# Places to look for libraries
################ 
#message(STATUS ${CMAKE_MODULE_PATH})
list(APPEND CMAKE_MODULE_PATH "/usr/share/SFML/cmake/Modules")
#message(STATUS ${CMAKE_MODULE_PATH})

################
# Packages
################
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
find_package(GLEW REQUIRED)
find_package(SFML REQUIRED system window graphics network audio)

################
# Included dirs
################
include_directories( ${OPENGL_INCLUDE_DIRS} )
include_directories( ${GLUT_INCLUDE_DIRS} )
include_directories( ${SFML_INCLUDE_DIR} )
include_directories( ${GLEW_INCLUDE_DIRS} )

################
# Project subdirectories
################
add_subdirectory("examples")