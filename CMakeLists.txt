cmake_minimum_required(VERSION 2.8)
project(MarkDown_CPP)

set(CMAKE_VERBOSE_MAKEFILE ON)
set(CMAKE_CXX_FLAGS "$ENV{CXXFLAGS} -rdynamic -O0 -ggdb -std=c++11 -Wall -Wno-deprecated -Werror -Wno-unused-function -Wno-builtin-macro-redefined")

include_directories(.)
include_directories(/usr/local/include)

link_directories(/usr/local/lib)

#set(LIB_SRC
#        src/
#)

#add_library(MarkDown_CPP SHARED ${LIB_SRC})

#set(LIB_LIB
#        MarkDown_CPP
#)

add_executable(tests tests/test.cpp)

SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)

