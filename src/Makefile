CC	:=	arm-linux-gnueabihf-gcc
#CFLAGS	:=	-g -O2 -pipe -Wall -I.
CFLAGS	:=	-g -O2 -pipe       -I.

all:
	$(CC)  $(CFLAGS)  -c -o y.tab.o y.tab.c
	$(CC)  $(CFLAGS)  -c -o lex.yy.o lex.yy.c
	$(CC)  $(CFLAGS)  -c -o alias.o alias.c
	$(CC)  $(CFLAGS)  -c -o boa.o boa.c
	$(CC)  $(CFLAGS)  -c -o buffer.o buffer.c
	$(CC)  $(CFLAGS)  -c -o cgi.o cgi.c
	$(CC)  $(CFLAGS)  -c -o cgi_header.o cgi_header.c
	$(CC)  $(CFLAGS)  -c -o config.o config.c
	$(CC)  $(CFLAGS)  -c -o escape.o escape.c
	$(CC)  $(CFLAGS)  -c -o get.o get.c
	$(CC)  $(CFLAGS)  -c -o hash.o hash.c
	$(CC)  $(CFLAGS)  -c -o ip.o ip.c
	$(CC)  $(CFLAGS)  -c -o log.o log.c
	$(CC)  $(CFLAGS)  -c -o mmap_cache.o mmap_cache.c
	$(CC)  $(CFLAGS)  -c -o pipe.o pipe.c
	$(CC)  $(CFLAGS)  -c -o queue.o queue.c
	$(CC)  $(CFLAGS)  -c -o read.o read.c
	$(CC)  $(CFLAGS)  -c -o request.o request.c
	$(CC)  $(CFLAGS)  -c -o response.o response.c
	$(CC)  $(CFLAGS)  -c -o select.o select.c
	$(CC)  $(CFLAGS)  -c -o signals.o signals.c
	$(CC)  $(CFLAGS)  -c -o util.o util.c
	$(CC)  $(CFLAGS)  -c -o sublog.o sublog.c
	$(CC)  $(CFLAGS)  -c -o timestamp.o timestamp.c
	$(CC)  -o boa y.tab.o lex.yy.o alias.o boa.o buffer.o cgi.o cgi_header.o config.o escape.o get.o hash.o ip.o log.o \
		mmap_cache.o pipe.o queue.o read.o request.o response.o select.o signals.o util.o sublog.o timestamp.o -g 
	$(CC)  $(CFLAGS)  -c -o index_dir.o index_dir.c
	$(CC)  -o boa_indexer index_dir.o escape.o -g 

clean:
	rm -f *.o boa_indexer boa
