cmake_minimum_required(VERSION 3.10)

project(LBRClientTemplate)

add_executable(${PROJECT_NAME} MyLBRApp.cpp MyLBRClient.cpp)

target_include_directories(${PROJECT_NAME}
        PUBLIC
            ${CMAKE_CURRENT_SOURCE_DIR}
)

target_link_libraries(${PROJECT_NAME}
        PUBLIC
            FRI::libFRIClient
)