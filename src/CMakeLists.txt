add_library(integratorxx 
  spherical_factory.cxx 
  radial_factory.cxx
  s2_factory.cxx
)

if(MSVC)
    # MSVC does not include <cmath> constants, unless _USE_MATH_DEFINES is defined.
    target_compile_definitions(integratorxx PUBLIC _USE_MATH_DEFINES)
    # Set the exception handling model (allows "throw"; if using add_compile_options form, set this *before* adding targets)
    target_compile_options(integratorxx PUBLIC "/EHsc")
endif()
