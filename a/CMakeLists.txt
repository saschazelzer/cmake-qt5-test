find_package(Qt5Core REQUIRED)

add_library(a a.cpp)
target_link_libraries(a Qt5::Core)

