cmake_minimum_required(VERSION 3.20)
project(CppIDE LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt6 COMPONENTS
    Core
    Gui
    Widgets
    Concurrent
    Network
    Process
    REQUIRED
)

set(PROJECT_SOURCES
    src/main.cpp
    src/mainwindow.h
    src/mainwindow.cpp
    src/editor/codeeditor.h
    src/editor/codeeditor.cpp
    src/editor/syntaxhighlighter.h
    src/editor/syntaxhighlighter.cpp
    src/ui/sidebar.h
    src/ui/sidebar.cpp
    src/ui/explorer.h
    src/ui/explorer.cpp
    src/ui/terminal.h
    src/ui/terminal.cpp
    src/ui/bottombar.h
    src/ui/bottombar.cpp
    src/git/gitmanager.h
    src/git/gitmanager.cpp
    src/autocomplete/autocompleter.h
    src/autocomplete/autocompleter.cpp
    src/autocomplete/parser.h
    src/autocomplete/parser.cpp
    src/resources/resources.qrc
)

add_executable(CppIDE ${PROJECT_SOURCES})

target_link_libraries(CppIDE
    Qt6::Core
    Qt6::Gui
    Qt6::Widgets
    Qt6::Concurrent
    Qt6::Network
    Qt6::Process
)

target_include_directories(CppIDE PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/src
    ${CMAKE_CURRENT_SOURCE_DIR}/src/editor
    ${CMAKE_CURRENT_SOURCE_DIR}/src/ui
    ${CMAKE_CURRENT_SOURCE_DIR}/src/git
    ${CMAKE_CURRENT_SOURCE_DIR}/src/autocomplete
)
