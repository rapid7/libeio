AC_PREREQ(2.59)
AC_INIT([libeio], [1.0])
AC_CONFIG_SRCDIR([eio.h])
AC_CONFIG_HEADERS([config.h])
AM_INIT_AUTOMAKE

AM_INIT_AUTOMAKE([subdir-objects foreign])
AC_CONFIG_MACRO_DIR([m4])
AM_MAINTAINER_MODE

AC_GNU_SOURCE

AC_PROG_LIBTOOL

AC_PROG_CC

AC_EGREP_CPP(we_are_using_clang,
[
#include <unistd.h>
#ifdef __clang__
we_are_using_clang
#endif
],
[AC_MSG_RESULT([yes])
IS_CLANG="yes"],
[AC_MSG_RESULT([no])])

if test x"$IS_CLANG" == x"yes" ; then
	CFLAGS="$CFLAGS -Wno-implicit-function-declaration"
fi

m4_include([m4/libeio.m4])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
