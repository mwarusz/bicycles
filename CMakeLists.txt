cmake_minimum_required(VERSION 2.8.6) # for CMakePushCheckState
project(bicycles CXX C)

enable_testing()

#search for libcloudphxx
find_package(libcloudph++)
if (NOT libcloudph++_FOUND)
  message(FATAL_ERROR "libclouphxx++ not found")
endif()

# search for libmpdata
find_package(libmpdata++)
if (NOT libmpdataxx_FOUND)
  message(FATAL_ERROR "libmpdata++ not found")
endif()


add_subdirectory(drawbicyc)
add_subdirectory(src) 
add_subdirectory(tests)
