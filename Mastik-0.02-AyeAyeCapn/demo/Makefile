FILES=$(wildcard *.c)
TARGETS=$(FILES:.c=)
OBJS=${FILES:.c=.o}
CFLAGS=-g -std=gnu99 -I../src
LDFLAGS=-L../src/ -g
LDLIBS=-lmastik -lelf -lbfd 


all: ${TARGETS}

${TARGETS}: %: %.o 
	${CC} ${LDFLAGS} -o $@ $@.o ${LDLIBS}


clean:
	rm -f ${TARGETS} ${OBJS} *.sig out

distclean: clean
	rm Makefile
