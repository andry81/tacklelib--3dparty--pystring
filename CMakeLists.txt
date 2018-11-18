cmake_minimum_required(VERSION 3.0)

include(Common)

project("pystring")

set(PROJECT_LIB_NAME pystring)


file(GLOB_RECURSE all_headers ${CMAKE_CURRENT_LIST_DIR}/pystring.h*)
file(GLOB_RECURSE all_sources ${CMAKE_CURRENT_LIST_DIR}/pystring.c*)

add_library(${PROJECT_LIB_NAME} STATIC ${all_headers};${all_sources})

initialize_library_target_defaults(${PROJECT_LIB_NAME} "32bit")

source_groups_from_dir_list("Header Files" FILES ${CMAKE_CURRENT_LIST_DIR} *.h*)
source_groups_from_dir_list("Source Files" FILES ${CMAKE_CURRENT_LIST_DIR} *.c*)

if(GCC)
  add_target_compile_properties(${PROJECT_LIB_NAME} *
    -Wall -Wextra -Wshadow -Wconversion -Wcast-qual -Wformat=2
  )
endif()
