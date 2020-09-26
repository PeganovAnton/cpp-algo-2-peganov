.PHONY: all clean install uninstall
		
all: program
		
clean:
	rm -rf program *.o	
program.o: program.cpp mylib.hpp
	g++ -c -o program.o program.cpp
mylib.o: mylib.cpp mylib.hpp
	g++ -c -o mylib.o mylib.cpp
program: program.o mylib.o
	g++ -o program program.o mylib.o
install:
	install ./program /usr/local/bin
uninstall:
	rm -rf /usr/local/bin/program
