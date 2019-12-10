cmake_minimum_required(VERSION 2.8)

project(crc8)

if(NOT CRC8_ROOT)
  message(FATAL_ERROR "CRC8_ROOT must be set to the location of crc8 sources.")
else()
  message(STATUS "crc8 sources in ${CRC8_ROOT}")
endif()

# set source files
set(crc8_SRCS
    ${CRC8_ROOT}/crc8.c
  )

# set lib
add_library(crc8
    ${crc8_SRCS}
)

target_include_directories(crc8 PUBLIC "${CRC8_ROOT}")

set(INS_TARGETS
    crc8
)

# Install
install(TARGETS ${INS_TARGETS}
    RUNTIME DESTINATION bin
    LIBRARY DESTINATION lib
    ARCHIVE DESTINATION lib
)
