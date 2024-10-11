INCDIR =../include
OBJDIR = ./obj
SRCDIR = ./

CC = gcc
FLAGS = 

_DEPS = 
DEPS  = $(patsubst %, $(INCDIR)/%, $(_DEPS))

_OBJS = main.o
OBJS  = $(patsubst %, $(OBJDIR)/%, $(_OBJS))

_SRCS = main.c
SRCS  = $(patsubst %, $(SRCDIR)/%, $(_SRCS))

$(OBJDIR)/%.o: $(SRCS) $(DEPS)
	$(CC) -c -o $@ $< $(FLAGS)

bin/app: $(OBJS)
	$(CC) -o $@ $^ $(FLAGS)

.PHONY: clean

clean:
	rm -f $(OBJDIR)/*.o *~ core $(INCDIR)/*~ 