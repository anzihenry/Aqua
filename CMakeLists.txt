cmake_minimum_required(VERSION 3.22)
project(Aqua)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_PREFIX_PATH "/usr/local/opt/qt@5/")


find_package(Qt5 COMPONENTS
        Core
        Gui
        Widgets
        REQUIRED)

include_directories(/usr/local/include)
link_directories(/usr/local/lib)
add_executable(Aqua main.cpp)

target_link_libraries(Aqua
        Qt5::Core
        Qt5::Gui
        Qt5::Widgets
        )

