# 📚 Libft - My 42 Core Library

Welcome to my **Libft** repository! This project was part of the **42 curriculum**, where I implemented my own version of essential C standard library functions. It served as a foundation for future projects at 42.

---

## **✅ Project Validation**
- **Validated on:** December 1, 2023  
- **Final Score:** 124/100  
  - Achieved **bonus part** 🎉  
  - One corrector mistakenly gave **123 instead of 125**, leading to an unusual final score.

---

## **📜 Project Overview**
The goal of this project is to recreate essential functions from `<string.h>`, `<stdlib.h>`, and other standard libraries. Additionally, it includes a set of custom functions designed to extend standard C capabilities.

### **Requirements:**
- Must **not** use external libraries (except for `write()`).
- Must follow **Norminette** coding standards.
- No memory leaks allowed.
- Must include a `Makefile` with rules:
  - `all` (compile library)
  - `clean` (remove object files)
  - `fclean` (remove object files & archive)
  - `re` (recompile everything)

### **Components:**
✅ **Mandatory Part:** Reimplement standard C functions like `memset`, `bzero`, `strdup`, `atoi`, etc.  
🚀 **Bonus Part:** Implement linked list utilities (`t_list` struct and related functions).  

### **Key Concepts:**
- **Memory Manipulation:** Handling memory using pointers.
- **String Manipulation:** Implementing and optimizing string operations.
- **Linked Lists:** Creating and managing linked list structures.

---

## **📂 Project Structure**
```
42-Libft/
│── ft_atoi.c               # Convert a string to an integer
│── ft_bzero.c              # Zero out memory
│── ft_calloc.c             # Allocate and zero-initialize memory
│── ft_isalnum.c            # Check if a character is alphanumeric
│── ft_isalpha.c            # Check if a character is alphabetic
│── ft_isascii.c            # Check if a character is an ASCII character
│── ft_isdigit.c            # Check if a character is a digit
│── ft_isprint.c            # Check if a character is printable
│── ft_itoa.c               # Convert integer to string
│── ft_memchr.c             # Locate a byte in memory
│── ft_memcmp.c             # Compare memory areas
│── ft_memcpy.c             # Copy memory area
│── ft_memmove.c            # Safer version of memcpy
│── ft_memset.c             # Fill memory with a constant byte
│── ft_putchar_fd.c         # Output a character to a file descriptor
│── ft_putendl_fd.c         # Output a string with newline to a file descriptor
│── ft_putnbr_fd.c          # Output a number to a file descriptor
│── ft_putstr_fd.c          # Output a string to a file descriptor
│── ft_split.c              # Split string into array of substrings by delimiter
│── ft_strchr.c             # Locate a character in a string
│── ft_strdup.c             # Duplicate a string
│── ft_striteri.c           # Apply function to each character of string with index
│── ft_strjoin.c            # Concatenate two strings with new memory allocation
│── ft_strlcat.c            # Concatenate with size limit (BSD-style)
│── ft_strlcpy.c            # Copy string with size limit
│── ft_strlen.c             # Get the length of a string
│── ft_strmapi.c            # Create new string by applying function to each char
│── ft_strncmp.c            # Compare strings up to a limit
│── ft_strnstr.c            # Locate a substring with a limit
│── ft_strrchr.c            # Locate last occurrence of a character
│── ft_strtrim.c            # Trim specified characters from beginning and end
│── ft_substr.c             # Extract substring from string
│── ft_tolower.c            # Convert character to lowercase
│── ft_toupper.c            # Convert character to uppercase
│── ft_lstadd_back_bonus.c  # Add a node at the end of a list
│── ft_lstadd_front_bonus.c # Add a node at the beginning of a list
│── ft_lstclear_bonus.c     # Clear an entire linked list
│── ft_lstdelone_bonus.c    # Delete a single node
│── ft_lstiter_bonus.c      # Apply function to each element of a list
│── ft_lstlast_bonus.c      # Get the last element of a list
│── ft_lstmap_bonus.c       # Apply function and create new list
│── ft_lstnew_bonus.c       # Create a new linked list node
│── ft_lstsize_bonus.c      # Count elements in a list
│── libft.h                 # Header file with function prototypes
│── Makefile                # Compilation instructions
```

---

## **🛠️ Installation & Usage**
To use the library in your project, clone the repository and compile it.

### **📥 Clone & Compile**
```sh
git clone https://github.com/osmaneb23/42-Libft.git
cd 42-Libft
make
```

### **📌 Compile with Your Project**
After compiling, link `libft.a` when compiling your own C files:

```sh
# Method 1: Using library flags
gcc your_file.c -L. -lft -o your_program

# Method 2: Directly specifying the library file
gcc your_file.c libft.a -o your_program
```