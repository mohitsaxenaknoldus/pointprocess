# Set minimum CMake's version required in order to build the project.
cmake_minimum_required(VERSION 3.19)

# Define Project name.
project(pointprocess)



# Set C++ standard to use.
set(CMAKE_CXX_STANDARD 20)

if (CMAKE_COMPILER_IS_GNUCC)
  add_compile_options(--coverage -O0)
endif()

# The add_subdirectory(source_dir) command adds a subdirectory to the build.
# The source_dir specifies the directory in which the source CMakeLists.txt and code files are located.
# Most of the times, we want to distinguish between the actual source code (located in src/)
#  and the tests (located in tests/)
# Each of these directories have a specific CMakeLists.txt file containing a set of directives and instructions
#  describing the project's source files and targets (executable, library, or both).
add_subdirectory(src)
enable_testing()
add_subdirectory(tests)


