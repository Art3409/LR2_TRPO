cmake_minimum_required(VERSION 3.10)
project(StackTest)

set(CMAKE_C_STANDARD 11)

# Включаем поддержку покрытия кода
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fprofile-arcs -ftest-coverage")
set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -fprofile-arcs -ftest-coverage")

add_executable(stack_test main.c stack.c)
