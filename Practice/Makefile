# -*Makefile*-
all: final
final: main.o name.o Uni.o
		gcc main.o name.o Uni.o -o final
main.o: main.c
		gcc -c main.c
name.o: name.c
		gcc -c name.c
Uni.o: Uni.c
		gcc -c Uni.c
clean:
		rm *.o final
