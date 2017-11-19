CC = gcc
CFLAGS = -O2 -Wall -I .

# This flag includes the Pthreads library on a Linux box.
# Others systems will probably require something different.
LIB = -lpthread

all: tiny cgi

tiny: tiny.c all.o
	$(CC) $(CFLAGS) -o tiny tiny.c all.o $(LIB)

csapp.o: csapp.c
	$(CC) $(CFLAGS) -c all.c

cgi:
	(cd cgi-bin; make)

clean:
	rm -f *.o tiny *~
	(cd cgi-bin; make clean)

