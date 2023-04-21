set(CMAKE_CXX_STANDARD 11)

add_executable(testPro_autogen test.cpp ${CMAKE_SOURCE_DIR}/helloWorld.h ${CMAKE_SOURCE_DIR}/helloWorld.cpp)

find_package(Catch2 CONFIG REQUIRED)
target_link_libraries(testPro_autogen PRIVATE Catch2::Catch2)
target_include_directories(testPro_autogen PRIVATE ${CMAKE_SOURCE_DIR})

enable_testing()
add_test(NAME testPro_autogen COMMAND testPro_autogen)
