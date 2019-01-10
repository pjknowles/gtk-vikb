cmake_minimum_required(VERSION 3.0)
project(gtk-vikb C)
find_package(gtk2 REQUIRED)
add_library(gtk-vikb MODULE vi.c)
target_include_directories(gtk-vikb PRIVATE ${GTK2_INCLUDE_DIRS})
target_link_libraries(gtk-vikb PUBLIC ${GTK2_LIBRARIES})

install(TARGETS gtk-vikb LIBRARY
        DESTINATION $ENV{HOME}/.gtk-2.0/modules
        )