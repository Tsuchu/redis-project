IDIR =../include
ODIR = ./obj
SDIR = ./
CC = gcc
CFLAGS = 

_DEPS = 
DEPS  = $(patsubst %, $(IDIR)/%, $(_DEPS))

_OBJS = main.o
OBJS  = $(patsubst %, $(ODIR)/%, $(_OBJS))

_SRCS = main.c
SRCS  = $(patsubst %, $(SDIR)/%, $(_SRCS))

$(ODIR)/%.o: $(SRCS) $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

bin/app: $(OBJS)
	$(CC) -o $@ $^ $(CFLAGS)

.PHONY: clean

clean:
	rm -f $(ODIR)/*.o *~ core $(INCDIR)/*~ 