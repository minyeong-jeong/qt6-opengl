cmake_minimum_required(VERSION 3.5)

project(testApp)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_BUILD_TYPE Debug)

find_package(Qt6 REQUIRED COMPONENTS Core Gui OpenGL)
qt_standard_project_setup()

qt_add_executable(main main.cpp)

target_compile_options(main PRIVATE -g)

set_target_properties(main PROPERTIES AUTOMOC TRUE)

target_link_libraries(main PRIVATE Qt6::Core Qt6::Gui Qt6::OpenGL)
