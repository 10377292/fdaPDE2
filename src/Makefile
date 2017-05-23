include Makefile.inc

CC=mpicc
CXX=mpic++

SRCS_BASIS=${wildcard *.cpp *.c}
SRCS_SHLIB=${SRCS_BASIS}

all: library 

library:
	MAKEFLAGS="CC=${CC} CXX=${CXX}" &&\
	R CMD SHLIB ${SRCS_SHLIB} -o fdaPDE.so

clean:
	rm -f *.o