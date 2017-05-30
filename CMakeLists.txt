cmake_minimum_required(VERSION 2.8)

project(levenshtein)

enable_testing()
find_package(GTest REQUIRED)
include_directories(${GTEST_INCLUDE_DIRS})

add_executable(${PROJECT_NAME} "main.cpp" "levenshtein.cpp")
target_link_libraries(${PROJECT_NAME} ${GTEST_BOTH_LIBRARIES})

add_test(RunAllTests ${PROJECT_NAME})
