cmake_minimum_required(VERSION 3.5)

project(opengl_template)

file(GLOB_RECURSE SOURCES "src/*")

add_executable(${PROJECT_NAME} ${SOURCES})

target_include_directories(${PROJECT_NAME}
    PRIVATE
        ${PROJECT_SOURCE_DIR}/include
)

add_subdirectory (${CMAKE_CURRENT_SOURCE_DIR}/deps/glfw)
target_link_libraries(${PROJECT_NAME} PRIVATE glfw)