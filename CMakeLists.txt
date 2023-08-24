cmake_minimum_required(VERSION 3.10)
project(tolua++)

set(CMAKE_C_STANDARD 11)
find_package(Lua REQUIRED)
include_directories(${LUA_INCLUDE_DIR})
include_directories(src/lib src/bin)
include_directories(${CMAKE_SOURCE_DIR}/include)

file(GLOB LIB_SRC src/lib/*.c)
add_library(tolua++ SHARED ${LIB_SRC})
install(TARGETS tolua++ DESTINATION /usr/local/lib)
install(FILES include/tolua++.h DESTINATION /usr/local/include)

file(GLOB BIN_SRC src/bin/*.c)
list(REMOVE_ITEM BIN_SRC "${CMAKE_SOURCE_DIR}/src/bin/toluabind_default.c")
add_executable(tolua++_bin ${BIN_SRC})
target_link_libraries(tolua++_bin tolua++ ${LUA_LIBRARIES})
set_target_properties(tolua++_bin PROPERTIES OUTPUT_NAME tolua++)
install(TARGETS tolua++_bin DESTINATION /usr/local/bin)

