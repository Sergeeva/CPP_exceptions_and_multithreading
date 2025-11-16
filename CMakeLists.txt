cmake_minimum_required(VERSION 3.19.0)

set (PROJECT_NAME gdb_workshop)
project(${PROJECT_NAME})

# настраиваем стандарт С++
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Установка режима сборки
#set(CMAKE_BUILD_TYPE Debug)

# устанавливаем флаги сборки
set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")

# настраиваем каталоги сборки
set(CMAKE_INCLUDE_CURRENT_DIR OFF)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})
list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

# раздельные каталоги для debug и release сборок
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_RELEASE ${CMAKE_BINARY_DIR}/release)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_DEBUG   ${CMAKE_BINARY_DIR}/debug)


## part 3
add_executable(task1 src/task3_1.cpp)
add_executable(task2 src/task3_2.cpp)
add_executable(task3 src/task3_3_races.cpp)
add_executable(task4 src/task3_3_deadlock.cpp)
