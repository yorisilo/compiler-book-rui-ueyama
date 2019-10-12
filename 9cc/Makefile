CFLAGS=-std=c11 -g -static

9cc: main.o
	$(CC) $? $(LDFLAGS) -o $@

asm: main.c
	$(CC) $? -S -masm=intel -o main.s

test: 9cc
	./test.sh

print: main.c
	echo $@ # $@ にはルールが入る
	echo $? # $? にはルールの後ろの引数が入る

clean:
	rm -f 9cc *.o *~ tmp*

.PHONY: test clean
