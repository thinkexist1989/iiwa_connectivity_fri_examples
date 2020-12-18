cmake_minimum_required(VERSION 3.10)

project(LBRJointSineOverlay)

add_executable(${PROJECT_NAME} LBRJointSineOverlayApp.cpp LBRJointSineOverlayClient.cpp)

target_include_directories(${PROJECT_NAME}
        PRIVATE
            ${CMAKE_CURRENT_SOURCE_DIR}
)

target_link_libraries(${PROJECT_NAME}
        PRIVATE
            FRI::libFRIClient
)