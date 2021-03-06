
set(LIBSTEPEDITOR_SRCS
    STEPfile.cc 
    STEPfile.inline.cc 
    cmdmgr.cc 
    dispnode.cc 
    dispnodelist.cc 
    instmgr.cc 
    mgrnode.cc 
    mgrnodearray.cc 
    mgrnodelist.cc 
    needFunc.cc 
    SdaiHeaderSchema.cc
    SdaiHeaderSchemaAll.cc
    SdaiHeaderSchemaInit.cc
    SdaiSchemaInit.cc
)

SET(LIBSTEPEDITOR_PRIVATE_HDRS
    STEPfile.h 
    cmdmgr.h 
    dispnode.h 
    dispnodelist.h 
    editordefines.h 
    instmgr.h 
    mgrnode.h 
    mgrnodearray.h 
    mgrnodelist.h 
    needFunc.h 
    SdaiHeaderSchema.h
    SdaiHeaderSchemaClasses.h
    SdaiSchemaInit.h
    seeinfodefault.h
)

include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${SCL_SOURCE_DIR}/src/base
    ${SCL_SOURCE_DIR}/src/cldai
    ${SCL_SOURCE_DIR}/src/clstepcore
    ${SCL_SOURCE_DIR}/src/clutils
)

SCL_ADDLIB(stepeditor "${LIBSTEPEDITOR_SRCS}" "stepcore stepdai steputils base")
