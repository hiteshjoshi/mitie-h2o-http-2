#
# This is a CMake makefile.  You can find the cmake utility and
# information about it at http://www.cmake.org
#

cmake_minimum_required(VERSION 2.6)



set(project_name main)
set(source
   main.c
   )


PROJECT(${project_name})


include(/usr/local/lib/mitielib/mitielib/cmake)
INCLUDE_DIRECTORIES(./h2o/include)
INCLUDE_DIRECTORIES(./openssl/include)
INCLUDE_DIRECTORIES(./libuv/include)


ADD_EXECUTABLE(${project_name} ${source})
TARGET_LINK_LIBRARIES(${project_name} mitie)
