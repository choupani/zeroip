
CC= cc

PREFIX = ../out/bin
INSTALL_PROGRAM = install -c -m 555 -o bin -g bin

SRCS   = main.c

CFLAGS= -O

OBJ =  $(SRCS:%.c=%.o)

XNAME =	zero

all: $(XNAME)

.c.o:
	$(CC) $(CFLAGS) -c $*.c -o $*.o

clean:
	rm -f $(OBJ) $(XNAME)

$(XNAME):$(OBJ)
	$(CC) $(CFLAGS) -o $@ $(OBJ) $(LIBS)

install:	zero
	$(INSTALL_PROGRAM) zero $(PREFIX)/
