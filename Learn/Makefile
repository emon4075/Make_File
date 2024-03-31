CFLAGS = -Wno-implicit-function-declaration

all: final

final: main.o hello.o
	@echo "Linking and Producing the Final File"
	gcc $(CFLAGS) main.o hello.o -o final

main.o: main.c
	@echo "Compiling the Main File"
	gcc $(CFLAGS) -c main.c

hello.o: hello.c
	@echo "Compiling the Hello File"
	gcc $(CFLAGS) -c hello.c

clean:
	@echo "Removing the Object Files and Final Executable"
	rm -f main.o hello.o final

