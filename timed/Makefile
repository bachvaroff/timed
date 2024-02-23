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

all: timed

timed: acksend.o byteorder.o candidate.o cksum.o correct.o master.o measure.o networkdelta.o readmsg.o slave.o timed.o
	$(LINK) $^ $(LDPOSTFLAGS0) -o $@

install: timed
	mkdir -p /usr/local/bin
	cp ./timed /usr/local/bin/

clean:
	rm -f *.o timed

