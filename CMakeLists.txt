cmake_minimum_required(VERSION 3.21)

project(vscodecmake LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt6 COMPONENTS Widgets REQUIRED)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)

qt_add_executable(main
    main.cpp
)
target_link_libraries(main PRIVATE Qt6::Widgets)
