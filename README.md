# Makefiles in C Programming

Makefiles are a crucial component in the development of C programs, aiding in automating the build process. They provide a structured way to define dependencies and commands for compiling and linking source code, simplifying the process of managing large projects with multiple files.

## Basic Structure of a Makefile

A Makefile consists of rules, each defining how to build a specific target. The structure typically follows this format:


- **Target**: Represents the file or action to be generated.
- **Dependencies**: Files or actions that must be completed before the target can be built.
- **Commands**: Shell commands to execute in order to build the target.


## Explanation:

- **CC**: Compiler command.
- **CFLAGS**: Compiler flags for debugging, warnings, etc.
- **TARGET**: Name of the executable.
- **SRCS**: List of C source files.
- **OBJS**: Object files derived from source files.
- **all**: Default target to build the executable.
- **$(TARGET)**: Rule to build the target executable.
- **%.o**: Rule to compile individual source files into object files.
- **clean**: Rule to remove compiled files.


## How to Use

1. **Writing**: Create a file named `Makefile` (or with `.mk` extension) in the project directory.
2. **Defining Targets**: Specify the targets, dependencies, and commands for building.
3. **Executing**: Run `make` command in the terminal to execute the Makefile.

## Tools Used

- **Text Editor**: NeoVim
- **Terminal**: Zsh
- **Compiler**: gcc


## Example Makefile

```make
# Example Makefile for a C program

# Compiler and flags
CC = gcc
CFLAGS = -Wall -Wextra -std=c99

# Target executable
TARGET = myprogram

# Source files
SRCS = main.c utils.c

# Object files
OBJS = $(SRCS:.c=.o)

# Default target
all: $(TARGET)

# Rule to build the target
$(TARGET): $(OBJS)
    $(CC) $(CFLAGS) -o $@ $^

# Rule to compile source files
%.o: %.c
    $(CC) $(CFLAGS) -c $< -o $@

# Clean rule
clean:
    rm -f $(OBJS) $(TARGET)
