INCLUDE(test_macros)
INCLUDE_DIRECTORIES(${CMAKE_BINARY_DIR}/fem/src)

CONFIGURE_FILE( MGDynamicsTransient.sif MGDynamicsTransient.sif COPYONLY)

file(COPY ELMERSOLVER_STARTINFO mesh3d DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/")

ADD_ELMER_TEST(mgdyn_transient_loss LABELS whitney transient)
