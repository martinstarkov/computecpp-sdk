project(FluidApp)

set(SOURCES
  "${CMAKE_CURRENT_SOURCE_DIR}/main.cpp"
  "${CMAKE_CURRENT_SOURCE_DIR}/fluid.cpp")

ci_make_app(
  APP_NAME "Fluid"
  SOURCES "${SOURCES}"
  LIBRARIES "${OpenCL_LIBRARIES}"
  CINDER_PATH "${CINDER_PATH}")

add_sycl_to_target(
    TARGET "Fluid"
    SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/fluid.cpp")
