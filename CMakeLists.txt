cmake_minimum_required(VERSION 3.16)
project(ImGui)

add_library(ImGui imconfig.h
                    imgui.h
                    imgui.cpp
                    imgui_draw.cpp
                    imgui_internal.h
                    imgui_widgets.cpp
                    imgui_tables.cpp
                    imstb_rectpack.h
                    imstb_textedit.h
                    imstb_truetype.h
                    imgui_demo.cpp)

set(imgui_macro "__declspec(dllexport)")
add_compile_definitions(IMGUI_API=${imgui_macro}) 


install(TARGETS ImGui RUNTIME DESTINATION /bin/${CMAKE_PROJECT_NAME})