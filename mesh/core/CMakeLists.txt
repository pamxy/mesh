file(GLOB ALL_SOURCE *.h *.cpp)

source_group("\\" FILES ${ALL_SOURCE})

include_directories(${CMAKE_CURRENT_BINARY_DIR})

add_library(Core STATIC ${ALL_SOURCE})
add_library(mesh.Core ALIAS Core)

set_target_properties(Core PROPERTIES OUTPUT_NAME mesh-core)
