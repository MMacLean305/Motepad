cmake_minimum_required(VERSION 3.16)
project(Motepad LANGUAGES CXX)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
find package(Qt REQUIRED COMPONENTS Widgets)
qt_standard_project_setup()
qt_add_executable(Motepad
    src/main.cpp
    src/MainWindow.cpp
    include/MainWindow.h
)
target_link_libraries(Motepad PRIVATE Qt6::Widgets)
target_include_directories(Motepad PRIVATE include)
