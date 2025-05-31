cmake_minimum_required(VERSION 3.10)
project(distributed_sgd VERSION 0.1 LANGUAGES CXX)

# --------------------------------------------
# 1) Set C++ standard to C++17 (required)
# --------------------------------------------
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# --------------------------------------------
# 2) Tell CMake where to find header files
#    (public headers live in include/)
# --------------------------------------------
include_directories(${PROJECT_SOURCE_DIR}/include)

# --------------------------------------------
# 3) Add any compiler flags you like (optional)
#    For example, to enable all warnings:
#    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -pedantic")
# --------------------------------------------
# set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -pedantic")

# --------------------------------------------
# 4) Declare the main executable target
#    We’ll point it to src/main.cpp
# --------------------------------------------
add_executable(distributed_sgd
    src/main.cpp
)

# --------------------------------------------
# 5) If you later add more source files, list them here:
#    add_executable(distributed_sgd
#        src/main.cpp
#        src/sgd.cpp
#        src/importance_sampling.cpp
#        …
#    )
# --------------------------------------------

# (Optional) If you later link against libraries, you can add:
# target_link_libraries(distributed_sgd PRIVATE <some_library>)
