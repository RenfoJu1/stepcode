
set(LIBSTEPUTILS_SRCS
    Str.cc 
    dirobj.cc 
    gennode.cc 
    gennodelist.cc 
    gennodearray.cc 
    scl_hash.cc 
    errordesc.cc 
)

SET(LIBSTEPUTILS_PRIVATE_HDRS
    dirobj.h 
    errordesc.h 
    gennodearray.h 
    gennode.h 
    gennodelist.h 
    scldir.h 
    scl_hash.h 
    stat.h 
    Str.h 
    str_list.h
)

include_directories(
    ${SCL_SOURCE_DIR}/src/base
    ${SCL_BINARY_DIR}/include
    ${CMAKE_CURRENT_SOURCE_DIR}
)

SCL_ADDLIB(steputils "${LIBSTEPUTILS_SRCS}" "base")

IF(MINGW OR MSVC OR BORLAND)
    TARGET_LINK_LIBRARIES(steputils shlwapi.lib)
ENDIF()
