cmake_minimum_required(VERSION 3.9)
project(example_cmake_custom_command)

file(GLOB SOURCE_FILES "src/*.src")

add_custom_command(
 OUTPUT  output.txt
 COMMAND cat ${SOURCE_FILES} | tee
 ARGS    -a output.txt
 DEPENDS ${SOURCE_FILES}
 COMMENT "Append contents of input to output"
)

add_custom_target(do_custom ALL
 DEPENDS output.txt
 SOURCES ${SOURCE_FILES}
)
