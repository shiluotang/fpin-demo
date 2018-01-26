ACLOCAL_AMFLAGS = -I m4

AM_CPPFLAGS = -Wall
AM_CFLAGS	= -mthumb \
			  -mcpu=cortex-m0 \
			  -Os -flto \
			  -ffunction-sections -fdata-sections
AM_CXXFLAGS =
AM_LDFLAGS	= \
			  -T $(top_srcdir)/ldscripts/gcc.ld \
			  -Wl,--gc-sections \
			  -Wl,-Map=fpin.map \
			  -u _scanf_float \
			  -u _print_float

noinst_PROGRAMS = fpin
fpin_SOURCES = ./src/fpin.c \
			   ./src/asm/startup_ARMCM0.S

fpin_LDFLAGS = $(AM_LDFLAGS)

EXTRA_DIST = \
			  $(top_srcdir)/ldscripts/gcc.ld \
			  $(top_srcdir)/ldscripts/mem.ld \
			  $(top_srcdir)/ldscripts/multi-ram.ld \
			  $(top_srcdir)/ldscripts/nokeep.ld
