# Simple Makefile for building the myhello library

CC = gcc
CFLAGS = -fPIC -shared
TARGET = libmyhello.so

all: $(TARGET)

$(TARGET): myhello.o
	$(CC) $(CFLAGS) -o $(TARGET) myhello.o

myhello.o: myhello.c
	$(CC) -c myhello.c

install:
	mkdir -p $(DESTDIR)/usr/lib $(DESTDIR)/usr/include
	install -m 0755 $(TARGET) $(DESTDIR)/usr/lib/
	install -m 0644 myhello.h $(DESTDIR)/usr/include/

clean:
	rm -f *.o $(TARGET)

