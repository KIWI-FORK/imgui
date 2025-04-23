set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# set thrid_party imgui dependeicy 
# if the subdirectory, DIR need set as set(IMGUI_DIR "${CMAKE_SOURCE_DIR}/third_party/imgui")
# https://github.com/ocornut/imgui/blob/master/examples/example_glfw_wgpu/CMakeLists.txt
set(IMGUI_DIR ${CMAKE_CURRENT_SOURCE_DIR})
include_directories(${IMGUI_DIR})
add_library(imgui STATIC
  ${IMGUI_DIR}/backends/imgui_impl_glfw.cpp
  ${IMGUI_DIR}/backends/imgui_impl_wgpu.cpp
  ${IMGUI_DIR}/imgui.cpp
  ${IMGUI_DIR}/imgui_draw.cpp
  ${IMGUI_DIR}/imgui_tables.cpp
  ${IMGUI_DIR}/imgui_widgets.cpp
)
