cmake_minimum_required (VERSION 3.10)

################
# Project
################ 
project (opengl_test)


################
# Places to look for libraries
################ 
#set (CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}/SFML/cmake-modules/")

set (SFML_INCLUDE_DIR "/usr/include/SFML")

################
# Packages
################
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
find_package(SFML REQUIRED system window graphics network audio)

################
# Included dirs
################
include_directories( ${OPENGL_INCLUDE_DIRS}  ${GLUT_INCLUDE_DIRS} )
include_directories( ${SFML_INCLUDE_DIR} )

################
# Executables
################
add_executable(sanity_1 sanity_1.cpp)
add_executable(opengl_hello_world opengl_hello_world.cpp)
add_executable(opengl_example2 opengl_example2.cpp)
add_executable(opengl_example3 opengl_example3.cpp)

################
# Link libraries
################
target_link_libraries(opengl_hello_world ${OPENGL_LIBRARIES} )
target_link_libraries(opengl_example2 ${OPENGL_LIBRARIES} ${GLUT_LIBRARY} ${SFML_LIBRARIES} ${SFML_DEPENDENCIES} )
target_link_libraries(opengl_example3 ${OPENGL_LIBRARIES} ${GLUT_LIBRARY} ${SFML_LIBRARIES} ${SFML_DEPENDENCIES} )

