if(MSVC)
    # MSVC does not include <cmath> constants, unless _USE_MATH_DEFINES is defined.
    add_compile_definitions(_USE_MATH_DEFINES)
    # Set the exception handling model (allows "throw"; if using add_compile_options form, set this *before* adding targets)
    add_compile_options("/EHsc")
endif()

add_library(integratorxx 
  spherical_factory.cxx 
  radial_factory.cxx
  s2_factory.cxx
)
