cmake_minimum_required( VERSION 2.8 )
project( lc CXX )

file( GLOB SRCS RELATIVE ${CMAKE_HOME_DIRECTORY} ${CMAKE_HOME_DIRECTORY}/src/*.cxx )
file( GLOB HDRS RELATIVE ${CMAKE_HOME_DIRECTORY} ${CMAKE_HOME_DIRECTORY}/src/*.hxx )
list( REMOVE_ITEM SRCS src/main.cxx dummy_item )
add_library( ${CMAKE_PROJECT_NAME} SHARED ${SRCS} ${HDRS} )
