# Copyright (C) 2006 International Business Machines and others.
# All Rights Reserved.
# This file is distributed under the Eclipse Public License.

## $Id$

# Author:  Andreas Waechter           IBM    2006-04-13

AUTOMAKE_OPTIONS = foreign

if COIN_HAS_OSI
SUBDIRS = OsiVol
endif

########################################################################
#                               libVol                                 #
########################################################################

# Name of the library compiled in this directory.  We want it to be installed
# in $libdir
lib_LTLIBRARIES = libVol.la

# List all source files for this library, including headers
libVol_la_SOURCES = VolVolume.cpp VolVolume.hpp

# This is for libtool (on Windows)
libVol_la_LDFLAGS = $(LT_LDFLAGS)

########################################################################
#                            Additional flags                          #
########################################################################


# Here list all include flags, relative to this "srcdir" directory.  This
# "cygpath" stuff is necessary to compile with native compilers on Windows.
# "top_srcdir" refers to the basic directory for the main package that is
# being compiled.
AM_CPPFLAGS = ${COINUTILS_CFLAGS}

# This line is necessary to allow VPATH compilation
DEFAULT_INCLUDES = -I. -I`$(CYGPATH_W) $(srcdir)` -I$(top_builddir)/inc

########################################################################
#                Headers that need to be installed                     #
########################################################################

# Here list all the header files that are required by a user of the library,
# and that therefore should be installed in 'include/coin'
includecoindir = $(includedir)/coin
includecoin_HEADERS = VolVolume.hpp
