# SPDX-License-Identifier: BSD-3-Clause
# Copyright Contributors to the OpenEXR Project.

add_executable(HalfTest
  main.cpp
  testArithmetic.cpp
  testBitPatterns.cpp
  testClassification.cpp
  testError.cpp
  testFunction.cpp
  testLimits.cpp
  testSize.cpp
  testToFloat.cpp
)

target_link_libraries(HalfTest Half)
set_target_properties(HalfTest PROPERTIES
  RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)
add_test(NAME Half COMMAND $<TARGET_FILE:HalfTest>)
