add_library(midi STATIC
	sdl_midi.c
)

include_directories(${SDL2_INCLUDE_DIRS})
include_directories(../../../Engine/src/)