cmake_Minimum_required(VERSION 3.10)
project("SCServo")

file(GLOB hdrs *.h)
file(GLOB srs *.cpp)

add_library(${PROJECT_NAME} STATIC ${hdrs} ${srs})

install(FILES ${hdrs} DESTINATION include/${PROJECT_NAME})

install(TARGETS ${PROJECT_NAME}
        ARCHIVE DESTINATION lib
        LIBRARY DESTINATION lib
        RUNTIME DESTINATION bin)