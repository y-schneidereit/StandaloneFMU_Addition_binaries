cmake_minimum_required (VERSION 3.2)

project (simulator)

add_executable(simulator
  include/fmi2Functions.h
  include/fmi2FunctionTypes.h
  include/fmi2TypesPlatform.h

  src/simulator.c
)

target_include_directories(simulator PUBLIC
  include
  model/binaries/win64
)

target_link_libraries(simulator C:/Users/schyan01/github/StandaloneFMU_Addition_binaries/model/binaries/win64/Addition_binaries.dll)
