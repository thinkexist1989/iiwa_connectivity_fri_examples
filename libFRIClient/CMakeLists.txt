cmake_minimum_required(VERSION 3.10)

project(libFRIClient)

# 加载src文件夹下所有的.cpp和.c文件
file(GLOB SOURCES
        "src/**/*.c"
        "src/**/*.cpp")


############################################################
# Create a library
############################################################

add_library(${PROJECT_NAME} STATIC
        ${SOURCES}
)

add_library(FRI::libFRIClient ALIAS ${PROJECT_NAME})

target_include_directories(${PROJECT_NAME}
        PUBLIC
            ${PROJECT_SOURCE_DIR}/include
            ${PROJECT_SOURCE_DIR}/src/base
            ${PROJECT_SOURCE_DIR}/src/client_lbr
            ${PROJECT_SOURCE_DIR}/src/connection
            ${PROJECT_SOURCE_DIR}/src/nanopb-0.2.8
            ${PROJECT_SOURCE_DIR}/src/protobuf
            ${PROJECT_SOURCE_DIR}/src/protobuf_gen
)
