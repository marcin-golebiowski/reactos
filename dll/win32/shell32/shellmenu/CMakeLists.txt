PROJECT(SHELL)

set_cpp(WITH_RUNTIME)

add_definitions(-DUNICODE -D_UNICODE)

include_directories(${REACTOS_SOURCE_DIR}/sdk/lib/atl)

list(APPEND SOURCE
    CMenuBand.cpp
    CMenuDeskBar.cpp
    CMenuFocusManager.cpp
    CMenuSite.cpp
    CMenuToolbars.cpp
    CMergedFolder.cpp
    CStartMenu.cpp)

add_library(shellmenu ${SOURCE})
add_dependencies(shellmenu xdk psdk)
