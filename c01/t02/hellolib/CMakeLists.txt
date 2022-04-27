add_library(hellolib STATIC hello.cpp)
target_include_directories(hellolib PUBLIC .) # 简化写法