#
# Copyright (c) 2018 Linaro Limited
#
# SPDX-License-Identifier: Apache-2.0
#

if(CONFIG_LIBHELIXMP3)
zephyr_library_named(libhelix-mp3)
zephyr_include_directories(
    libhelix-mp3/src/pub
)

FILE(GLOB HelixMP3_real_src
        libhelix-mp3/src/real/*.c)

        
zephyr_library_sources(
	libhelix-mp3/src/mp3dec.c
    libhelix-mp3/src/mp3tabs.c
    ${HelixMP3_real_src}
)
endif()