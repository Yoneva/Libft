# Libft

A custom C library that reimplements standard C library functions, created as part of the 42 curriculum.

## Description

Libft is a foundational project that involves coding a C library with commonly used functions. This library will serve as a base for future 42 projects. The project is divided into mandatory functions (standard C library reimplementations) and bonus functions (linked list manipulation).

## Features

### Part 1 - Libc Functions
Reimplementation of standard C library functions:

**Character checks:**
- `ft_isalpha` - Check if character is alphabetic
- `ft_isdigit` - Check if character is a digit
- `ft_isalnum` - Check if character is alphanumeric
- `ft_isascii` - Check if character is ASCII
- `ft_isprint` - Check if character is printable
- `ft_islower` - Check if character is lowercase
- `ft_toupper` - Convert character to uppercase
- `ft_tolower` - Convert character to lowercase

**String manipulation:**
- `ft_strlen` - Calculate string length
- `ft_strchr` - Locate character in string
- `ft_strrchr` - Locate character in string (from end)
- `ft_strncmp` - Compare strings up to n bytes
- `ft_strnstr` - Locate substring in string
- `ft_strlcpy` - Copy string with size limit
- `ft_strlcat` - Concatenate strings with size limit
- `ft_strdup` - Duplicate string

**Memory functions:**
- `ft_memset` - Fill memory with constant byte
- `ft_bzero` - Zero a byte string
- `ft_memcpy` - Copy memory area
- `ft_memmove` - Copy memory area (handles overlap)
- `ft_memchr` - Scan memory for character
- `ft_memcmp` - Compare memory areas
- `ft_calloc` - Allocate and zero memory

**Conversion:**
- `ft_atoi` - Convert string to integer

### Part 2 - Additional Functions

- `ft_substr` - Extract substring from string
- `ft_strjoin` - Concatenate two strings
- `ft_strtrim` - Trim characters from string
- `ft_split` - Split string by delimiter
- `ft_itoa` - Convert integer to string
- `ft_strmapi` - Apply function to each character (with index)
- `ft_striteri` - Apply function to each character (modify in place)
- `ft_putchar_fd` - Output character to file descriptor
- `ft_putstr_fd` - Output string to file descriptor
- `ft_putendl_fd` - Output string + newline to file descriptor
- `ft_putnbr_fd` - Output integer to file descriptor

### Bonus - Linked List Functions

- `ft_lstnew` - Create new list node
- `ft_lstadd_front` - Add node at beginning of list
- `ft_lstadd_back` - Add node at end of list
- `ft_lstsize` - Count list elements
- `ft_lstlast` - Get last list element
- `ft_lstdelone` - Delete single list node
- `ft_lstclear` - Delete entire list
- `ft_lstiter` - Iterate through list and apply function
- `ft_lstmap` - Create new list by applying function to each node

## Installation

Clone the repository:
```bash
git clone https://github.com/yourusername/libft.git
cd libft
```

## Compilation

Compile the library:
```bash
make
```

This will create `libft.a` static library.

### Available Make Rules

- `make` or `make all` - Compile mandatory functions
- `make bonus` - Compile mandatory + bonus functions
- `make clean` - Remove object files
- `make fclean` - Remove object files and library
- `make re` - Recompile entire library

## Usage

Include the header in your C files:
```c
#include "libft.h"
```

Compile your program with the library:
```bash
cc your_program.c libft.a -o your_program
```

### Example Usage

```c
#include "libft.h"
#include <stdio.h>

int main(void)
{
    char *str = ft_strdup("Hello, 42!");
    char *upper = ft_strmapi(str, ft_toupper);
    
    ft_putstr_fd(upper, 1);
    ft_putchar_fd('\n', 1);
    
    free(str);
    free(upper);
    return (0);
}
```

## Project Structure

```
.
├── Makefile
├── libft.h           # Header file with function prototypes
├── ft_*.c            # Mandatory function implementations
└── ft_*_bonus.c      # Bonus function implementations
```

## Technical Details

- **Language:** C
- **Compilation flags:** `-Wall -Wextra -Werror`
- **Compiler:** cc (gcc/clang)
- **Output:** `libft.a` (static library)
- **Norm:** Code follows 42's coding standards (Norminette)

## Author

**amsbai** - 42 Student

## License

This project is part of the 42 School curriculum.

## Acknowledgments

This project is part of the 42 curriculum, teaching fundamental programming concepts and C library functions implementation.
