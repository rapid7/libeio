AUTOMAKE_OPTIONS = foreign no-dependencies

VERSION_INFO = 1:0

EXTRA_DIST = LICENSE Changes autogen.sh etp.c

man_MANS = eio.3

ACLOCAL_AMFLAGS = -I m4

include_HEADERS = eio.h

lib_LTLIBRARIES = libeio.la

libeio_la_SOURCES = eio.c ecb.h xthread.h config.h
libeio_la_LDFLAGS = -version-info $(VERSION_INFO)

noinst_PROGRAMS = demo

demo_LDADD = $(abs_top_builddir)/libeio.a
demo_SOURCES = demo.c
