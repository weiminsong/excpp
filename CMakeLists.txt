cmake_minimum_required(VERSION 2.8)
include(CMakeToolsHelpers OPTIONAL)
project(ExCpp C CXX)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 11)

function(add_exercise CHAPTER EXERCISE)
	set(EXECUTABLE ${CHAPTER}/${EXERCISE}.cpp)
	add_executable(${EXERCISE} ${EXECUTABLE})
	set_target_properties(${EXERCISE} PROPERTIES LINKER_LANGUAGE CXX)
endfunction(add_exercise)

add_exercise(statements Forwhile)
add_exercise(statements Atoi)
add_exercise(statements Itoa)
add_exercise(statements StripComments)

#add_exercise(expressions Parenthesize)
#add_exercise(expressions Read-pairs)
#add_exercise(expressions Bitwise)