bin_PROGRAMS = qperf

if RDMA
AM_CFLAGS = -Wall -O -DRDMA
if HAS_XRC
AM_CFLAGS += -DHAS_XRC=1
endif
qperf_SOURCES = qperf.c socket.c rds.c rdma.c support.c help.c qperf.h
qperf_LDADD = -libverbs
else
AM_CFLAGS = -Wall -O
qperf_SOURCES = qperf.c socket.c rds.c support.c help.c qperf.h
endif

man_MANS = qperf.1

#qperf.1: help.txt
#	./mkman >qperf.1

#help.c: help.txt
#if RDMA
#	./mkhelp.pl RDMA
#else
#	./mkhelp.pl
#endif

clean-local:
#	-rm -f qperf.1
