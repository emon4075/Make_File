all : final

final : Main.o Name.o Uni.o
	@echo "Linked"
	@gcc Main.o Name.o Uni.o -o final

Main.o : Main.c
	@echo "Generated Main"
	@gcc -c Main.c

Name.o : Name.c
	@echo "Generated Name"
	@gcc -c Name.c

Uni.o : Uni.c
	@echo "Generated Uni"
	@gcc -c Uni.c

clean : 
	@echo "Removing Files"
	@rm *.o final
