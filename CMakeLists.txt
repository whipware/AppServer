cmake_minimum_required(VERSION 3.10)

# set the project name
project(AppServer)


target_link_libraries(${PROJECT_NAME}
    PRIVATE
    "-losip2"
    "-losipparser2"
)


# add the executable
add_executable(${PROJECT_NAME} main.cpp)

