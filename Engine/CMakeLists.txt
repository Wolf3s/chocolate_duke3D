add_library(Engine STATIC
	src/cache.c
	src/display.c
	src/draw.c
	src/engine.c
	src/filesystem.c
	src/fixedPoint_math.c
	src/mmulti.c
	src/network.c
	src/tiles.c
)

include_directories(${SDL2_INCLUDE_DIRS})
include_directories(src/)