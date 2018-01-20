ADD_SUBDIRECTORY(libtransport)

add_custom_target(test $<TARGET_FILE:libtransport_test> WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/tests_output)
add_custom_target(extended_test $<TARGET_FILE:libtransport_test> COMMAND python ${CMAKE_CURRENT_SOURCE_DIR}/start.py WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/tests_output)
