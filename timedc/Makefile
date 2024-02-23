CC=cc
CFLAGS=-m32 -O0
INCLUDE=-I.
LDFLAGS=-m32
LDPOSTFLAGS0=-lbsd
SOFLAGS=
DEBUG=-g
COMPILE=$(CC) $(DEBUG) $(INCLUDE) $(CFLAGS)
LINK=$(CC) $(DEBUG) $(LDFLAGS)
LINKSO=$(CC) $(DEBUG) $(SOFLAGS)
LD_LIBRARY_PATH=

.c.o:
	$(COMPILE) -c $< -o $@

all: timedc

timedc: cmds.o cmdtab.o timedc.o ../timed/measure.o ../timed/byteorder.o ../timed/cksum.o broken.o
	$(LINK) $^ $(LDPOSTFLAGS0) -o $@

install: timedc
	mkdir -p /usr/local/bin
	cp ./timedc /usr/local/bin/

clean:
	rm -f *.o timedc

