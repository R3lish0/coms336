# Compiler and flags
CXX = g++
CXXFLAGS = -I./include

# Default source file
SRC = ./src/main.cc

# Output file
TARGET = ./make/output

# Rule for building the target
$(TARGET): main.o
	$(CXX) ./make/main.o -o $(TARGET)

# Rule for compiling the object file
main.o: $(SRC) ./include/rtweekend.h
	$(CXX) $(CXXFLAGS) -c $(SRC) -o ./make/main.o

# Bench target
.PHONY: bench
bench: SRC = ./src/bench.cc
bench: $(TARGET)

.PHONY: mac
mac: CXX = g++-14
mac: $(TARGET)

# Rule for compiling the object file for bench
bench.o: $(SRC) ./include/rtweekend.h
	$(CXX) $(CXXFLAGS) -c $(SRC) -o ./make/bench.o

# Clean rule
.PHONY: clean
clean:
	rm -f ./make/*
	rm image.ppm
