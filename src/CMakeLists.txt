FILE(GLOB_RECURSE SOURCES "*.cpp")
FILE(GLOB_RECURSE HEADERS "*.h")

IF(CMAKE_GENERATOR MATCHES "Xcode")
  add_executable(simplelexer ${SOURCES} ${HEADERS})
ELSE()
  add_executable(simplelexer ${SOURCES})
ENDIF()

target_link_libraries(simplelexer PRIVATE ${llvm_libs})
