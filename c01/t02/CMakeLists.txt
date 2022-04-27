cmake_minimum_required(VERSION 3.10)
project(hellocmake LANGUAGES CXX)

# 静态库写法
# add_library(hellolib STATIC hello.cpp)
# add_executable(a.out main.cpp)
# target_link_libraries(a.out PUBLIC hellolib)

#动态库写法
# add_library(hellolib SHARED hello.cpp)
# add_executable(a.out main.cpp)
# target_link_libraries(a.out PUBLIC hellolib)

#hello.cpp移动到hellolib下
# add_subdirectory(hellolib) #添加sub dir

# add_executable(a.out main.cpp)
# target_link_libraries(a.out PUBLIC hellolib)
# target_include_directories(a.out PUBLIC hellolib) #target 包含 sub dir

#简化写法
add_subdirectory(hellolib)
add_executable(a.out main.cpp)
target_link_libraries(a.out PUBLIC hellolib)
