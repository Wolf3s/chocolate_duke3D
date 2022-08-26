cmake_minimum_required(VERSION 2.6)

project(chocolate-duke3d)
find_package(SDL2 REQUIRED)
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -DPLATFORM_UNIX")

add_subdirectory(Engine/)
add_subdirectory(Game/src/audiolib/)
add_subdirectory(Game/src/midi/)

link_directories(
	${CMAKE_SOURCE_DIR}/Game/src/audiolib/
	${CMAKE_SOURCE_DIR}/Game/src/midi/
	${CMAKE_SOURCE_DIR}/Engine/
)

add_executable(chocolate-duke3d
	Game/src/actors.c
	Game/src/animlib.c
	Game/src/config.c
	Game/src/console.c
	Game/src/control.c
	Game/src/cvar_defs.c
	Game/src/cvars.c
	Game/src/game.c
	Game/src/gamedef.c
	Game/src/global.c
	Game/src/keyboard.c
	Game/src/menues.c
	Game/src/player.c
	Game/src/premap.c
	Game/src/rts.c
	Game/src/scriplib.c
	Game/src/sector.c
	Game/src/sounds.c
)

include_directories(${SDL2_INCLUDE_DIRS})
include_directories(Engine/src/)

target_link_libraries(chocolate-duke3d audio midi Engine SDL2 SDL2_mixer)
