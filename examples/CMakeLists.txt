################
# Executables
################
add_executable(sanity_1			sanity_1.cpp)
add_executable(opengl_example1	opengl_example1.cpp)
add_executable(opengl_example2	opengl_example2.cpp)
add_executable(opengl_example3	opengl_example3.cpp)
add_executable(opengl_example4	opengl_example4.cpp)

################
# Link libraries
################
target_link_libraries(opengl_example1		${OPENGL_LIBRARIES} ${GLUT_LIBRARY}  )
target_link_libraries(opengl_example2		${OPENGL_LIBRARIES} ${GLUT_LIBRARY} ${GLEW_LIBRARIES} ${SFML_LIBRARIES} ${SFML_DEPENDENCIES} )
target_link_libraries(opengl_example3		${OPENGL_LIBRARIES} ${GLUT_LIBRARY} ${GLEW_LIBRARIES} ${SFML_LIBRARIES} ${SFML_DEPENDENCIES} )
target_link_libraries(opengl_example4		${OPENGL_LIBRARIES} ${GLUT_LIBRARY} ${GLEW_LIBRARIES} ${SFML_LIBRARIES} ${SFML_DEPENDENCIES} )