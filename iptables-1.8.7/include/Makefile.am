# -*- Makefile -*-

include_HEADERS =
nobase_include_HEADERS = xtables.h xtables-version.h

if ENABLE_LIBIPQ
include_HEADERS += libipq/libipq.h
endif

nobase_include_HEADERS += \
	libiptc/ipt_kernel_headers.h libiptc/libiptc.h \
	libiptc/libip6tc.h libiptc/libxtc.h libiptc/xtcshared.h

uninstall-hook:
	dir=${includedir}/libiptc; { \
		test ! -d "$$dir" && test ! -f "$$dir" && test ! -r "$$dir"; \
	} || rmdir -p --ignore-fail-on-non-empty "$$dir"
