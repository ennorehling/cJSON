cmake_minimum_required(VERSION 2.6)
project (cjson C)

SET (LIB_SRC cJSON.c cJSON.h)
ADD_LIBRARY (cjson ${LIB_SRC})

set (CJSON_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR} CACHE INTERNAL "cJSON headers")
set (CJSON_LIBRARIES cjson CACHE INTERNAL "cJSON libraries")
