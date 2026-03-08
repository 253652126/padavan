# trunk/user/msd_lite/Makefile
# Pure native build for Padavan (no OpenWrt, no CMake)

all: msd_lite

msd_lite:
	$(CC) $(CFLAGS) -std=c99 -D_GNU_SOURCE \
		-Isrc -Isrc/lib -Isrc/utils \
		-o $@ \
		src/main.c \
		src/lib/*.c \
		src/utils/*.c \
		-lpthread

install:
	mkdir -p $(INSTALLDIR)/usr/bin
	cp msd_lite $(INSTALLDIR)/usr/bin/
	mkdir -p $(INSTALLDIR)/etc_ro
	cp msd_lite.conf $(INSTALLDIR)/etc_ro/

clean:
	rm -f msd_lite

.PHONY: all install clean
