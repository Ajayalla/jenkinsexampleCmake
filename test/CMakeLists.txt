set(CMAKE_CXX_STANDARD 11)

add_executable(testPro.dir test.cpp ${CMAKE_SOURCE_DIR}/helloWorld.h ${CMAKE_SOURCE_DIR}/helloWorld.cpp)

find_package(Catch2 CONFIG REQUIRED)
target_link_libraries(testPro.dir PRIVATE Catch2::Catch2)
target_include_directories(testPro.dir PRIVATE ${CMAKE_SOURCE_DIR})

enable_testing()
add_test(NAME testPro.dir COMMAND testPro.dir)
