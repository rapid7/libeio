AUTOMAKE_OPTIONS = foreign no-dependencies

VERSION_INFO = 1:0

EXTRA_DIST = LICENSE Changes autogen.sh etp.c eio.3

man_MANS = eio.3

ACLOCAL_AMFLAGS = -I m4

include_HEADERS = eio.h

lib_LTLIBRARIES = libeio.la

libeio_la_SOURCES = eio.c ecb.h xthread.h config.h
libeio_la_LDFLAGS = -version-info $(VERSION_INFO)

if !HOST_WIN
noinst_PROGRAMS = demo
demo_LDADD = libeio.la
demo_SOURCES = demo.c
endif
