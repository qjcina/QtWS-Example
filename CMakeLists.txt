cmake_minimum_required(VERSION 3.16)
project(com.qtws.weather LANGUAGES CXX)

option(CMAKE_AUTOMOC "Automoc" ON)
option(DESIGNER_BUILD "Enable designer build" OFF)

add_subdirectory(frontend)
add_subdirectory(backend_simulator)
add_subdirectory(designer)
add_subdirectory(imports)
if(NOT DESIGNER_BUILD)
    add_subdirectory(backend)
    add_subdirectory(server)
    add_subdirectory(application)
endif()
