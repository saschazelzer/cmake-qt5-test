cmake-qt5-test
==============

Testing CMake 2.8.12 features together with Qt5

### Project Structure

The project contains two libraries "a" and "b". "a" links to Qt5::Core and uses Qt5 headers in its public API. "b" links to "a" using `target_link_libraries` and includes a header from "a" which itself includes a Qt header.

### Problem

Without adding a `find_package(Qt5Core)` call in the scope of library "b", the include directories of the link interface of "a" are not properly set on target "b".

This means that "b" needs knowledge of "a"s dependencies.
