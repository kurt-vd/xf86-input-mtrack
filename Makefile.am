SOURCES_COMMON = \
	$(srcdir)/src/capabilities.c \
	$(srcdir)/src/gestures.c \
	$(srcdir)/src/hwstate.c \
	$(srcdir)/src/mconfig.c \
	$(srcdir)/src/mtouch.c \
	$(srcdir)/src/mtstate.c

@DRIVER_NAME@_drv_la_LTLIBRARIES = @DRIVER_NAME@_drv.la
@DRIVER_NAME@_drv_la_LDFLAGS = -module -avoid-version
@DRIVER_NAME@_drv_la_SOURCES = $(SOURCES_COMMON) \
	$(srcdir)/driver/mtrack.c \
	$(srcdir)/driver/mprops.c
@DRIVER_NAME@_drv_ladir = @inputdir@

noinst_PROGRAMS = mtrack-test
mtrack_test_SOURCES = $(SOURCES_COMMON) \
	$(srcdir)/tools/mtrack-test.c
mtrack_test_CFLAGS = $(AM_CFLAGS)

AM_CPPFLAGS = -I$(top_srcdir)/include/
AM_CFLAGS = $(XORG_CFLAGS)

.PHONY: ChangeLog INSTALL

INSTALL:
	$(INSTALL_CMD)

ChangeLog:
	$(CHANGELOG_CMD)

dist-hook: ChangeLog INSTALL
