CC = gcc
CFLAGS = -O3 -std=c23 -Wall -Werror

BIN = main

# $@: rule target
# $^: all rule requisites
# $<: first rule requisite

all: $(BIN)

$(BIN): temp/main.o temp/lib.o
	$(CC) $(CFLAGS) -o $@ $^

temp/main.o: src/main.c include/lib.h
	$(CC) $(CFLAGS) -c $< -o $@

temp/lib.o: src/lib.c include/lib.h
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -rf temp/* $(BIN)

.PHONY: all clean
