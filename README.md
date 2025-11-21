# 22101258-Assignment2-os
This repository contains the required programs and documentation for Assignment 2
- C source files for all exercises --- file1.c , file2.c , process_creation.c , simple_program.c
- makefile 
cc = gcc
cflags = -Wall -g

programs = process_creation output_program simple_program

all: $(programs)

process_creation: process_creation.c
	$(cc) $(cflags) process_creation.c -o process_creation

output_program: file1.c file2.c
	$(cc) $(cflags) file1.c file2.c -o output_program

simple_program: simple_program.c
	$(cc) $(cflags) simple_program.c -o simple_program

clean:
	rm -f $(programs)

