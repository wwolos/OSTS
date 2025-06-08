cmake_minimum_required(VERSION 3.16)
project(OSTS)

set(CMAKE_CXX_STANDARD 17)

include(FetchContent)
FetchContent_Declare(
  SFML
  GIT_REPOSITORY https://github.com/SFML/SFML.git
  GIT_TAG        2.6.1 # Or latest stable
)
FetchContent_MakeAvailable(SFML)

add_executable(OSTS  src/main.cpp)
target_include_directories(OSTS PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)
target_link_libraries(OSTS  sfml-graphics sfml-window sfml-system)
