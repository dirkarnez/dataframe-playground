cmake_minimum_required(VERSION 3.14)

project(dataframe-boilerplate)

set(dataframe_ROOT "P:/Downloads/cpp-libraries/DataFrame-V-1.5.0/build/DataFrame")

SET(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -static")

include_directories("${dataframe_ROOT}/include")

add_executable(${PROJECT_NAME}
    "src/main.cpp"
)

target_link_libraries(${PROJECT_NAME} "${dataframe_ROOT}/lib/libDataFrame.a")