cmake_minimum_required (VERSION 3.14)
project(Nagisa)

set(CMAKE_CXX_STANDARD 17)

add_subdirectory(dependencies/sleep_discord)

set(NAGISA_HEADERS
)
set(NAGISA_SOURCES
)
set(NAGISA_LINK_LIBRARIES
  sleepy-discord
)
set(NAGISA_EXECUTABLE_HEADERS
  ${NAGISA_HEADERS}
)
set(NAGISA_EXECUTABLE_SOURCES
  ${NAGISA_SOURCES}
  src/main.cpp
)
set(NAGISA_EXECUTABLE_LINK_LIBRARIES
  ${NAGISA_LINK_LIBRARIES}
)

add_executable(Nagisa ${NAGISA_EXECUTABLE_HEADERS} ${NAGISA_EXECUTABLE_SOURCES})

target_link_libraries(Nagisa ${NAGISA_EXECUTABLE_LINK_LIBRARIES})
