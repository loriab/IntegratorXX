add_library(integratorxx 
  spherical_factory.cxx 
  radial_factory.cxx
  s2_factory.cxx
)

if(MSVC)
    # MSVC does not include <cmath> constants, unless _USE_MATH_DEFINES is defined.
    add_compile_definitions(_USE_MATH_DEFINES)
endif()
