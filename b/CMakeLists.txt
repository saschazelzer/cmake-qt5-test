include_directories(${PROJECT_SOURCE_DIR}/a)

# enabling the line below will make it work, but "b" needs
# knowledge about the dependencies of "a"

#find_package(Qt5Core REQUIRED)

add_library(b b.cpp)
target_link_libraries(b a)

