# This file was generated automatically by configure.  Do not edit.
VPATH = .
links = 
host_alias = m68k-hp-bsd
host_cpu = m68k
host_vendor = hp
host_os = bsd
host_canonical = m68k-hp-bsd
target_alias = m68k-hp-bsd
target_cpu = m68k
target_vendor = hp
target_os = bsd
target_canonical = m68k-hp-bsd
host_makefile_frag = ../m68k-hp-bsd.mh
ALL=all.internal
# Copyright (C) 1989, 1992 Free Software Foundation, Inc.
# written by Douglas C. Schmidt (schmidt@ics.uci.edu)
# 
# This file is part of GNU GPERF.
# 
# GNU GPERF is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 1, or (at your option)
# any later version.
# 
# GNU GPERF is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with GNU GPERF; see the file COPYING.  If not, write to
# the Free Software Foundation, 675 Mass Ave, Cambridge, MA 02139, USA. 

srcdir = .

prefix = /usr/local

exec_prefix = $(prefix)
bindir = $(exec_prefix)/bin
libdir = $(exec_prefix)/lib

datadir = $(prefix)/lib
mandir = $(prefix)/man
man1dir = $(mandir)/man1
man2dir = $(mandir)/man2
man3dir = $(mandir)/man3
man4dir = $(mandir)/man4
man5dir = $(mandir)/man5
man6dir = $(mandir)/man6
man7dir = $(mandir)/man7
man8dir = $(mandir)/man8
man9dir = $(mandir)/man9
infodir = $(prefix)/info
includedir = $(prefix)/include
docdir = $(datadir)/doc

SHELL = /bin/sh

INSTALL = install -c
INSTALL_PROGRAM = $(INSTALL)
INSTALL_DATA = $(INSTALL)

AR = `if [ -f $${rootme}/../../binutils/ar ] ; \
	then echo $${rootme}/../../binutils/ar ; \
	else echo ar ; fi`

AR_FLAGS = qc
RANLIB = `if [ -f $${rootme}/../../binutils/ranlib ] ; \
	then echo $${rootme}/../../binutils/ranlib ; \
	else echo ranlib ; fi`

MAKEINFO = `if [ -f $${rootme}/../../texinfo/C/makeinfo ] ; \
	then echo $${rootme}/../../texinfo/C/makeinfo ; \
	else echo makeinfo ; fi`

CC = `if [ -f $${rootme}/../../gcc/gcc ] ; \
	then echo $${rootme}/../../gcc/gcc -B$${rootme}/../../gcc/ ; \
	else echo cc ; fi`
CXX = `if [ -f $${rootme}../gcc/gcc ] ; \
	then echo $${rootme}../gcc/gcc\\ -B$${rootme}../gcc/ ; \
	else echo gcc; fi`

CFLAGS = -g
CXXFLAGS = -g -O
XTRAFLAGS = `if [ -f $${rootme}/../../gcc/gcc ] ; \
	then echo -I$${rootme}/../../gcc/include ; \
	else echo ; fi`

IO_DIR = iostream

SUBDIRS = src tests

#### host and target dependent Makefile fragments come in here.
INSTALL = install -c
INSTALL_DATA = install -c -m 644
# RANLIB = ranlib
# Use -nostdinc++ flag if your version of gcc understands it.
NOSTDINC = # -nostdinc++

# If the C include files are C++-ready (with extern "C"),
# define: HAVE_CPLUS_EXTERN = 1 and: WRAP_C_INCLUDES =
# If not, define HAVE_CPLUS_EXTERN = 0, and do not define WRAP_C_INCLUDES here.
HAVE_CPLUS_EXTERN = 0

# Flags to pass to gen-params when building _G_config.h.
# For example: G_CONFIG_ARGS = size_t="unsigned long"
G_CONFIG_ARGS =
##

FLAGS_TO_PASS=\
	"prefix=$(prefix)" \
	"exec_prefix=$(exec_prefix)" \
	"tooldir=$(tooldir)" \
	"CC=$(CC)" \
	"CFLAGS=$(CFLAGS)" \
	"CXX=$(CXX)" \
	"CXXFLAGS=$(CXXFLAGS)" \
	"XTRAFLAGS=$(XTRAFLAGS)" \
	"AR=$(AR)" \
	"RANLIB=$(RANLIB)"

.NOEXPORT:
.PHONY: all
all:
	rootme=`pwd` ; export rootme ; cd src ; \
		$(MAKE) $(FLAGS_TO_PASS)

.PHONY: check
check:
	rootme=`pwd` ; export rootme ; cd tests ; \
		$(MAKE) $(FLAGS_TO_PASS) check

.PHONY: install
install:
	rootme=`pwd` ; export rootme ; cd src ; \
		$(MAKE) $(FLAGS_TO_PASS) install
	-parent=`echo $(man1dir)|sed -e 's@/[^/]*$$@@'`; \
	if [ -d $$parent ] ; then true ; else mkdir $$parent ; fi
	-if [ -d $(man1dir) ] ; then true ; else mkdir $(man1dir) ; fi
	$(INSTALL) $(srcdir)/gperf.1 $(man1dir)/gperf.1

.PHONY: info
info: gperf.info

gperf.info: gperf.texinfo
	$(MAKEINFO) -o gperf.info $(srcdir)/gperf.texinfo

.PHONY: install-info
install-info: gperf.info
	-parent=`echo $(infodir)|sed -e 's@/[^/]*$$@@'`; \
	if [ -d $$parent ] ; then true ; else mkdir $$parent ; fi
	-if [ -d $(infodir) ] ; then true ; else mkdir $(infodir) ; fi
	for i in *.info* ; do \
		$(INSTALL_DATA) $$i $(infodir)/$$i ; \
		chmod a-x $(infodir)/$$i ; \
	done

.PHONY: clean-info
clean-info:
	-rm -f *.info*

distrib: force
	cd ..; rm -f gperf.tar.Z; tar cvf gperf.tar gperf; compress gperf.tar;\
	       uuencode gperf.tar.Z < gperf.tar.Z > GSHAR

.PHONY: shar
shar: force
	cd ..; makekit -ngperf ./gperf ./gperf/* ./gperf/src/* ./gperf/tests/*


.PHONY: mostlyclean clean distclean realclean
.PHONY: do_mostlyclean do_clean do_distclean do_realclean
do_mostlyclean: force
	-rm -f \#* core *.o gperf.?? gperf.??s gperf.log gperf.toc \
	       gperf.*aux *inset.c *out gperf
do_clean: do_mostlyclean
do_distclean: do_clean
	rm -rf *~ config.status Makefile
do_realclean: do_distclean
	-rm -f gperf.info* depend
mostlyclean: do_mostlyclean
	@for D in $(SUBDIRS) ; do (cd $$D ; $(MAKE) mostlyclean); done 
clean: do_clean
	@for D in $(SUBDIRS) ; do (cd $$D ; $(MAKE) clean); done 
distclean:
	@for D in $(SUBDIRS) ; do (cd $$D ; $(MAKE) distclean); done
	@$(MAKE) do_distclean
realclean:
	@for D in $(SUBDIRS) ; do (cd $$D ; $(MAKE) realclean); done
	@$(MAKE) do_realclean

.PHONY: force
force:

# with the gnu make, this is done automatically.

Makefile: $(srcdir)/Makefile.in $(host_makefile_frag) $(target_makefile_frag)
	$(SHELL) ./config.status

