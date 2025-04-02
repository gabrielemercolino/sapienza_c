CC = gcc
CFLAGS = -O3 -std=c23 -Wall -Wextra -Werror -Iinclude

BIN = main

# $@: rule target
# $^: all rule requisites
# $<: first rule requisite

all: $(BIN)

$(BIN): main.o lib.o
	$(CC) $(CFLAGS) -o $@ ./*.o

main.o: src/main.c include/lib.h 
	$(CC) $(CFLAGS) -c $< -o $@

lib.o: src/lib.c include/lib.h
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -rf ./*.o $(BIN)

.PHONY: all clean
