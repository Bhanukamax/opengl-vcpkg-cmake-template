cmake_minimum_required(VERSION 3.10)

set(CMAKE_TOOLCHAIN_FILE "/home/bm/vc/vcpkg/scripts/buildsystems/vcpkg.cmake")
set(CMAKE_EXPORT_COMPILE_COMMANDS true)

# set the project name
project(Tutorial VERSION 1.0)


# Finding packages
# these are from vcpkg
#find_package(raylib CONFIG REQUIRED)
find_package(glfw3 CONFIG REQUIRED)
find_package(OpenGL REQUIRED)

# add the executable
add_executable(Tutorial src/test.cpp)

# linking
# vcpkg
#target_link_libraries(Tutorial PRIVATE OpenGL::GL)
target_link_libraries(Tutorial PRIVATE glfw)
#target_link_libraries(Tutorial PRIVATE opengl)


#target_link_libraries(Tutorial OpenGL::LGL)
#target_link_libraries(Tutorial OpenGL::GL)
target_link_libraries(Tutorial PRIVATE ${OPENGL_gl_LIBRARY})



#target_include_directories(Tutorial PRIVATE ${RAYLIB_INCLUDE_DIRS})
#target_link_libraries(Tutorial PRIVATE ${RAYLIB_LIBRARIES})

#target_link_libraries(Tutorial PRIVATE ${asdfasdfsd})
