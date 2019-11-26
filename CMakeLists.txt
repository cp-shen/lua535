cmake_minimum_required(VERSION 3.13)

project(lua_535)

set(CMAKE_CXX_STANDARD 14)

include_directories(include)

file(GLOB source_files
        src/lapi.c
        src/lauxlib.c
        src/lbaselib.c
        src/lbitlib.c
        src/lcode.c
        src/lcorolib.c
        src/lctype.c
        src/ldblib.c
        src/ldebug.c
        src/ldo.c
        src/ldump.c
        src/lfunc.c
        src/lgc.c
        src/linit.c
        src/liolib.c
        src/llex.c
        src/lmathlib.c
        src/lmem.c
        src/loadlib.c
        src/lobject.c
        src/lopcodes.c
        src/loslib.c
        src/lparser.c
        src/lstate.c
        src/lstring.c
        src/lstrlib.c
        src/ltable.c
        src/ltablib.c
        src/ltm.c
        src/lundump.c
        src/lutf8lib.c
        src/lvm.c
        src/lzio.c
        )

add_executable(lua_535
        ${source_files}
        src/lua.c
        )

add_executable(luac_535
        ${source_files}
        src/luac.c
        )

target_link_libraries(lua_535 m)

target_link_libraries(luac_535 m)
