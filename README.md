This repository holds the CMakeList.txt file for compiling the [CRC8](https://github.com/UlrikHjort/CRC8).

How to use:

1. Download the source code of both repositories, e.g.:

```
git clone https://github.com/madwyn/crc8-cmake.git
git clone https://github.com/UlrikHjort/CRC8.git
```

```
/crc8-cmake
/CRC8
CMakeLists.txt
```

2. In the `CMakeLists.txt`

```
set(CRC8_ROOT ${CMAKE_CURRENT_LIST_DIR}/CRC8)
add_subdirectory(crc8-cmake)
```

3. Link the target

```
target_link_libraries(example_app crc8)
```
