project(wxcharts)
cmake_minimum_required(VERSION 3.17)

include(cmake/pkg.cmake)

file(GLOB_RECURSE wxcharts-src src/*.cpp)
add_library(wxcharts ${wxcharts-src})
target_link_libraries(wxcharts wx::core wx::base)
target_include_directories(wxcharts PUBLIC include)
target_include_directories(wxcharts PRIVATE include/wx/charts)
