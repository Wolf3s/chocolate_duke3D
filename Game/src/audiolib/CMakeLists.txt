add_library(audio STATIC
	fx_man.c
	dsl.c
	ll_man.c
	multivoc.c
	mv_mix.c
	mvreverb.c
	nodpmi.c
	pitch.c
	user.c
	usrhooks.c
)

include_directories(${SDL2_INCLUDE_DIRS})
include_directories(../../../Engine/src/)