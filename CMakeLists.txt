cmake_minimum_required(VERSION 3.6)


set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include(cmake/HunterGate.cmake)

HunterGate(
    URL "https://github.com/n0k8t/hunter/archive/v0.19.137.1.tar.gz"
    SHA1 "f411b045dd72a16eb4cd9ff10abe59a49526f490"
)

project(pack)
hunter_add_package(nlohmann_json)
find_package(nlohmann_json CONFIG REQUIRED)

add_executable(pack ${CMAKE_CURRENT_SOURCE_DIR}/sources/pack.cpp)
target_link_libraries(pack nlohmann_json)
add_executable(unpack ${CMAKE_CURRENT_SOURCE_DIR}/sources/unpack.cpp)
target_link_libraries(unpack nlohmann_json)