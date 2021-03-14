cmake_minimum_required( VERSION 3.7 FATAL_ERROR )
set( CMAKE_VERBOSE_MAKEFILE ON )

project( sample-cinder-cmake-project )

get_filename_component( CINDER_PATH "${CMAKE_CURRENT_SOURCE_DIR}/third-party/Cinder" ABSOLUTE )
get_filename_component( APP_PATH "${CMAKE_CURRENT_SOURCE_DIR}/" ABSOLUTE )

include( "${CINDER_PATH}/proj/cmake/modules/cinderMakeApp.cmake" )

ci_make_app(
  APP_NAME    ${PROJECT_NAME}
  CINDER_PATH ${CINDER_PATH}
  SOURCES     ${APP_PATH}/src/main.cpp
  INCLUDES    ${APP_PATH}/include
  RESOURCES   ${APP_PATH}/assets/white.jpg
)
