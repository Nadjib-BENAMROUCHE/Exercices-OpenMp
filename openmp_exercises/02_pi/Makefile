.PHONY: clean run go debug release

PROG=pi
CC ?= gcc
FLAGS_OPENMP ?= -fopenmp -D READ_INPUT  #pour executer la partie READ_INPUT

release:
	$(CC) -Wall -g -lm $(FLAGS_OPENMP) -O3 ${PROG}.c -o ${PROG}.exe

debug:
	$(CC) -Wall -g -lm $(FLAGS_OPENMP) -O0 ${PROG}.c -o ${PROG}.exe

run go:
	./${PROG}.exe

clean:
	rm -f ${PROG}.exe ${PROG}.o *~
