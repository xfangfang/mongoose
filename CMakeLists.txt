cmake_minimum_required(VERSION 3.15)

add_library(mongoose STATIC ${CMAKE_CURRENT_SOURCE_DIR}/mongoose.c)

if (__SWITCH__)
    target_compile_options(mongoose PRIVATE -DMG_ARCH=10086)
endif()

target_include_directories(mongoose PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})