# 指定cmake的最小版本
cmake_minimum_required(VERSION 3.2)

# 指定项目的名称
project(CmakeTest)

file(GLOB_RECURSE HEAD_FILES
  ./src/*.h 

)
file(GLOB_RECURSE SRC_FILES
./src/*.cpp
)

set(ALL_FILES ${HEAD_FILES} ${SRC_FILES})

source_group("source" FILES ${SRC_FILES})
source_group("head" FILES ${HEAD_FILES})

# 指定可执行文件名称
add_executable(CmakeTest ${ALL_FILES})
