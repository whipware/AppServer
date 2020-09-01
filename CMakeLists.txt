cmake_minimum_required(VERSION 3.10)

# set the project name
project(AppServer)

link_directories(${CMAKE_SOURCE_DIR}/lib)
link_directories(/usr/local/lib)
find_package(system)

include_directories(/usr/local/include/losip2)

# add the executable
add_executable(${PROJECT_NAME} main.cpp)

target_link_libraries(${PROJECT_NAME}
    PRIVATE
    "-losip2"
    "-losipparser2"
)