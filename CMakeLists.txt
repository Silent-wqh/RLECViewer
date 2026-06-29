cmake_minimum_required(VERSION 3.15)
project(RLECViewer)

cmake_policy(SET CMP0091 NEW)
set(CMAKE_MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>")
set(CMAKE_MFC_FLAG 1) # Use MFC in a static library
add_compile_definitions(_MBCS WIN32 NDEBUG _WINDOWS)

add_executable(RLECViewer WIN32
    RLECViewer/NewMenu.cpp
    RLECViewer/NewMenuBar.cpp
    RLECViewer/Ntray.cpp
    RLECViewer/RLConfigDlg.cpp
    RLECViewer/RLECViewer.cpp
    RLECViewer/RLECViewerDlg.cpp
    RLECViewer/StdAfx.cpp
    RLECViewer/RLECViewer.rc
)
