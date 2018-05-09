PROJECT (t3Math)
cmake_minimum_required(VERSION 2.6)

INCLUDE_DIRECTORIES(
	"${CMAKE_SOURCE_DIR}/t3Math"
	"${CMAKE_SOURCE_DIR}"
)

FILE(GLOB t3Math_h "${CMAKE_SOURCE_DIR}/t3Math/*.h") 
SOURCE_GROUP("t3Math" FILES ${t3Math_h})

FILE(GLOB t3Math_cpp "${CMAKE_SOURCE_DIR}/t3Math/*.cpp") 
SOURCE_GROUP("t3Math" FILES ${t3Math_cpp})

# FILE(GLOB main_cpp "${CMAKE_SOURCE_DIR}/t3Math/*.cpp") 
# SOURCE_GROUP("Test" FILES ${main_cpp})

FILE(GLOB t3Math_test_h "${CMAKE_SOURCE_DIR}/test/*.h") 
SOURCE_GROUP("Test" FILES ${t3Math_test_h})

FILE(GLOB t3Math_test_cpp "${CMAKE_SOURCE_DIR}/test/*.cpp") 
SOURCE_GROUP("Test" FILES ${t3Math_test_cpp})

ADD_EXECUTABLE(t3Math ${main_cpp}
	${t3Math_h} ${t3Math_cpp}
	${t3Math_test_h} ${t3Math_test_cpp}
)