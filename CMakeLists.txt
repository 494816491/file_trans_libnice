cmake_minimum_required(VERSION 2.8)

project(file_trans_libnice)

set(LIBNICE_DIR "/home/ln/webrtc/libnice/_install")

include_directories(
    ${LIBNICE_DIR}/include/nice
    /usr/include/glib-2.0
    /usr/lib/x86_64-linux-gnu/glib-2.0/include/
    )
link_directories(
    /usr/lib/x86_64-linux-gnu/
    ${LIBNICE_DIR}/lib
    )
link_libraries(
    nice
    gio-2.0
    gobject-2.0
    glib-2.0
    pthread


    )



add_executable(${PROJECT_NAME} "main.cpp")
