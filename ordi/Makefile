Simple: Simple.y Simple.l
	bison -d Simple.y
	gcc -c Simple.tab.c
	flex Simple.l
	gcc -c lex.yy.c
	gcc -o Simple Simple.tab.o lex.yy.o -lm

clean: 
	rm *.tab.c
	rm *.tab.h
	rm *.yy.c
	rm *.o
	rm Simple