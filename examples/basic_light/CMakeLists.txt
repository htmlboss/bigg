add_executable( basic_light basic_light.cpp fs_basic_light.sc vs_basic_light.sc )
target_link_libraries( basic_light bigg )
set_target_properties( basic_light PROPERTIES FOLDER "examples" )

add_shader( vs_basic_light.sc VERTEX   OUTPUT ${CMAKE_CURRENT_BINARY_DIR}/shaders DX11_MODEL 5_0 GLSL 130 )
add_shader( fs_basic_light.sc FRAGMENT OUTPUT ${CMAKE_CURRENT_BINARY_DIR}/shaders DX11_MODEL 5_0 GLSL 130 )

configure_debugging( basic_light WORKING_DIR ${CMAKE_CURRENT_BINARY_DIR} )
