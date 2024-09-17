output: main.o 
	g++ ./make/main.o -o ./make/output

main.o: ./src/main.cc ./include/rtweekend.h
	g++ -I/include/rtweekend.h -c ./src/main.cc -o ./make/main.o


clean:
	rm ./make/* 
