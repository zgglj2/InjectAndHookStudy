cmake_minimum_required(VERSION 2.8)
project(LDPreloadHook)

set(CMAKE_CXX_STANDARD 11)

SET(CMAKE_BUILD_TYPE Debug)

set(SAMPLE_LIB_FILES LDPreloadHook.cpp)
add_library(LDPreloadHook SHARED ${SAMPLE_LIB_FILES})

set(TEST_HOOK_FILES TestLDPreloadHook.cpp)
add_executable(TestLDPreloadHook ${TEST_HOOK_FILES})
target_link_libraries(TestLDPreloadHook dl)
