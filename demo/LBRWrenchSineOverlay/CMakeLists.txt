cmake_minimum_required(VERSION 3.10)

project(LBRWrenchSineOverlay)

add_executable(${PROJECT_NAME} LBRWrenchSineOverlayClient.cpp LBRWrenchSineOverlayApp.cpp)

target_include_directories(${PROJECT_NAME}
        PUBLIC
            ${CMAKE_CURRENT_SOURCE_DIR}
)

target_link_libraries(${PROJECT_NAME}
        PUBLIC
            FRI::libFRIClient
)