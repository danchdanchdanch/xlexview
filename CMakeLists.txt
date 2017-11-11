cmake_minimum_required(VERSION 3.8)

project(xlexview)

set(SOURCE src/main.c src/parse.c src/list.c src/font.c)
set(IMPORTED_LIBS libX11)

include_directories(/usr/X11/include)

set(X11 /opt/x11/lib/libX11.dylib)

add_executable(${PROJECT_NAME} ${SOURCE})

target_link_libraries(${PROJECT_NAME} ${X11})

