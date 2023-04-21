set(CMAKE_CXX_STANDARD 11)

add_executable(testPro test.cpp ${CMAKE_SOURCE_DIR}/moc_predefs.h ${CMAKE_SOURCE_DIR}/mocs_compilation.cpp)

find_package(Catch2 CONFIG REQUIRED)
target_link_libraries(testPro PRIVATE Catch2::Catch2)
target_include_directories(testPro PRIVATE ${CMAKE_SOURCE_DIR})

enable_testing()
add_test(NAME testPro COMMAND testPro)
