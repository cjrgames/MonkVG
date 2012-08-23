#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.68])
AC_INIT([MonkVG], [1.1],[] )
AC_CONFIG_SRCDIR([glu/libtess/dict.c])

# Checks for programs.
LT_INIT
AM_INIT_AUTOMAKE([foreign])
AC_PROG_CXX
# Default to using C++
AC_LANG([C++])

# Checks for libGL
AC_CHECK_HEADERS([GL/gl.h GL/glu.h  GL/glew.h],[],[AC_MSG_FAILURE(Need OpenGL)])

# Checks for boost c++ libs
AC_CHECK_HEADERS([boost/ptr_container/ptr_map.hpp],[],[AC_MSG_FAILURE(Need Boost C++ Libraries)])

AC_CHECK_LIB(GL,glFlush, [], [AC_MSG_FAILURE(Need OpenGL Library - libGL)])
AC_CHECK_LIB(GLU,gluTessBeginPolygon, [], [AC_MSG_FAILURE(Need OpenGL Utility Library - libGLU)])
AC_CHECK_LIB(GLEW,glOrtho, [], [AC_MSG_FAILURE(Need OpenGL Extension Wrangler Library - libGLEW)])

# Keep the correct libtool macros in-tree
AC_CONFIG_MACRO_DIR([m4])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
