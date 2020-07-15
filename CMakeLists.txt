cmake_minimum_required(VERSION "3.7.1")

project("HelloWorld")

# This {PROJECT_NAME} value is "Hello World" defined above
add_executable("${PROJECT_NAME}" "main.cpp")

install(TARGETS "${PROJECT_NAME}" DESTINATION bin) #${CMAKE_INSTALL_PREFIX}/bin
install(FILES "main.cpp" DESTINATION src) #${CMAKE_INSTALL_PREFIX}/src

include(CTest)

add_test("test1" "${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}") #CMAKE_CURRENT_BINARY_DIR is build directory