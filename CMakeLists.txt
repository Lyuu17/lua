set(lua_SOURCES
    "src/lib/lauxlib.c"
    "src/lib/lbaselib.c"
    "src/lib/ldblib.c"
    "src/lib/liolib.c"
    "src/lib/lmathlib.c"
    "src/lib/loadlib.c"
    "src/lib/lstrlib.c"
    "src/lib/ltablib.c"
    "src/lapi.c"
    "src/lcode.c"
    "src/ldebug.c"
    "src/ldo.c"
    "src/ldump.c"
    "src/lfunc.c"
    "src/lgc.c"
    "src/llex.c"
    "src/lmem.c"
    "src/lobject.c"
    "src/lopcodes.c"
    "src/lparser.c"
    "src/lstate.c"
    "src/lstring.c"
    "src/ltable.c"
    "src/ltests.c"
    "src/ltm.c"
    "src/lundump.c"
    "src/lvm.c"
    "src/lzio.c"
)
set_source_files_properties(${lua_SOURCES} PROPERTIES LANGUAGE CXX)

add_library(lua STATIC ${lua_SOURCES})
target_include_directories(lua PUBLIC include PRIVATE src)
set_target_properties(lua PROPERTIES LINKER_LANGUAGE CXX)
