
ADD_BII_TARGETS()
SET_TARGET_PROPERTIES(${BII_tests_TARGET} PROPERTIES OUTPUT_NAME tests)

IF(APPLE)
    TARGET_COMPILE_OPTIONS(${BII_BLOCK_TARGET} INTERFACE "-std=c++11 -stdlib=libc++")
ELSEIF (WIN32 OR UNIX)
    TARGET_COMPILE_OPTIONS(${BII_BLOCK_TARGET} INTERFACE "-std=c++11")
ENDIF(APPLE)