packextrasdir=@docdir@
SUBDIRS = src etc man po
EXTRA_DIST=         \
BUGS                \
README.md            \
ChangeLog           \
AUTHORS.md           \
THANKS	            \
COPYING							\
INSTALL             \
NEWS                \
TODO

packextras_DATA=$(EXTRA_DIST)

PACKAGE = @PACKAGE@
VERSION = @VERSION@

ACLOCAL_AMFLAGS = --install -I m4

distdir = $(PACKAGE)-$(VERSION)

## begin gnulib module configmake

# Listed in the same order as the GNU makefile conventions, and
# provided by autoconf 2.59c+ or 2.70.
# The Automake-defined pkg* macros are appended, in the order
# listed in the Automake 1.10a+ documentation.
src/coreutils/configmake.h: Makefile
	$(AM_V_GEN)rm -f $@-t && \
	{ echo '/* DO NOT EDIT! GENERATED AUTOMATICALLY! */'; \
	  echo '#define PREFIX "$(prefix)"'; \
	  echo '#define EXEC_PREFIX "$(exec_prefix)"'; \
	  echo '#define BINDIR "$(bindir)"'; \
	  echo '#define SBINDIR "$(sbindir)"'; \
	  echo '#define LIBEXECDIR "$(libexecdir)"'; \
	  echo '#define DATAROOTDIR "$(datarootdir)"'; \
	  echo '#define DATADIR "$(datadir)"'; \
	  echo '#define SYSCONFDIR "$(sysconfdir)"'; \
	  echo '#define SHAREDSTATEDIR "$(sharedstatedir)"'; \
	  echo '#define LOCALSTATEDIR "$(localstatedir)"'; \
	  echo '#define RUNSTATEDIR "$(runstatedir)"'; \
	  echo '#define INCLUDEDIR "$(includedir)"'; \
	  echo '#define OLDINCLUDEDIR "$(oldincludedir)"'; \
	  echo '#define DOCDIR "$(docdir)"'; \
	  echo '#define INFODIR "$(infodir)"'; \
	  echo '#define HTMLDIR "$(htmldir)"'; \
	  echo '#define DVIDIR "$(dvidir)"'; \
	  echo '#define PDFDIR "$(pdfdir)"'; \
	  echo '#define PSDIR "$(psdir)"'; \
	  echo '#define LIBDIR "$(libdir)"'; \
	  echo '#define LISPDIR "$(lispdir)"'; \
	  echo '#define LOCALEDIR "$(localedir)"'; \
	  echo '#define MANDIR "$(mandir)"'; \
	  echo '#define MANEXT "$(manext)"'; \
	  echo '#define PKGDATADIR "$(pkgdatadir)"'; \
	  echo '#define PKGINCLUDEDIR "$(pkgincludedir)"'; \
	  echo '#define PKGLIBDIR "$(pkglibdir)"'; \
	  echo '#define PKGLIBEXECDIR "$(pkglibexecdir)"'; \
	} | sed '/""/d' > $@-t && \
	mv -f $@-t $@

BUILT_SOURCES = src/coreutils/configmake.h

## end   gnulib module configmake
