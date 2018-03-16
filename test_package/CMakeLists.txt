project(PackageTest C)
cmake_minimum_required(VERSION 2.8.12)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

add_executable(server server.c)
target_link_libraries(server ${CONAN_LIBS})

add_executable(client client.c)
target_link_libraries(client ${CONAN_LIBS})
