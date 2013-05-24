cmake_minimum_required(VERSION 2.6)
project (cjson C)

IF(CMAKE_COMPILER_IS_GNUCC)
    SET(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -pedantic -Wall -Werror -Wno-unknown-pragmas -Wstrict-prototypes -Wpointer-arith -Wno-char-subscripts -Wno-long-long")
ELSE(CMAKE_COMPILER_IS_GNUCC)
    MESSAGE(STATUS "Unknown compiler ${CMAKE_C_COMPILER_ID}")
ENDIF(CMAKE_COMPILER_IS_GNUCC)

SET (LIB_SRC cJSON.c cJSON.h)
ADD_LIBRARY (cjson ${LIB_SRC})

set (CJSON_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR} CACHE INTERNAL "cJSON headers")
set (CJSON_LIBRARIES cjson CACHE INTERNAL "cJSON libraries")
