all:
	gcc -W -Wall -Wextra -pedantic -std=c17 -fPIC -c util.c -o util.o
	gcc -shared -fPIC -o libutil.so util.o

	gcc -W -Wall -Wextra -pedantic -std=c17 -c main.c -o main.o
	gcc main.o -L. -lutil -o lg03

run:all 
	clear
	@LD_LIBRARY_PATH=$(CURDIR) ./lg03

clean:
	rm -f main.o
	rm -f util.o
	rm -f libutil.so
	rm -f lg03
	
