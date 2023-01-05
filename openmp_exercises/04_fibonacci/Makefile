.PHONY: clean run go debug release

PROG=fibonacci
CC ?= gcc
FLAGS_OPENMP ?= -fopenmp

release:
	$(CC) -Wall -g $(FLAGS_OPENMP) -O3 ${PROG}.c -o ${PROG}.exe

debug:
	$(CC) -Wall -g $(FLAGS_OPENMP) -O0 ${PROG}.c -o ${PROG}.exe

run go:
	OMP_NUM_THREDS=4 ./${PROG}.exe < input

clean:
	rm -f ${PROG}.exe ${PROG}.o *~
