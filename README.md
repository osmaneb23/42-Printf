# 📝 ft_printf - Custom printf Implementation

Welcome to my **ft_printf** repository! This project is part of the **42 curriculum**, where I've implemented my own version of the essential `printf()` function. This project expanded my knowledge of variadic functions and string formatting in C.

---

## **✅ Project Validation**
- **Validated on:** March 25, 2024
- **Final Score:** 100/100 

---

## **📜 Project Overview**
The goal of this project was to recreate the standard `printf()` function from `<stdio.h>` library. This implementation handles various data type conversions and formats them according to specified conversion specifiers.

### **Requirements:**
- Must handle variadic arguments.
- Cannot use the original printf's buffer management.
- Must follow **Norminette** coding standards.
- No memory leaks allowed.
- Must include a `Makefile` with rules:
  - `all` (compile library)
  - `clean` (remove object files)
  - `fclean` (remove object files & archive)
  - `re` (recompile everything)
- **Allowed functions:**
  - `malloc`
  - `free`
  - `write`
  - `va_start`
  - `va_arg`
  - `va_copy`
  - `va_end`
- My own Libft was also allowed.

### **Required Conversions:**
- **%c**: Print a single character.
- **%s**: Print a string.
- **%p**: Print a void pointer in hexadecimal format.
- **%d**: Print a decimal (base 10) number.
- **%i**: Print an integer in base 10.
- **%u**: Print an unsigned decimal number.
- **%x**: Print a number in lowercase hexadecimal format.
- **%X**: Print a number in uppercase hexadecimal format.
- **%%**: Print a percent sign.

### **Key Concepts & Skills Developed:**
- **Variadic Functions:** Implementing functions that handle a variable number of arguments.
- **String Formatting:** Converting various data types to string representation.
- **Memory Management:** Ensuring proper allocation and freeing of memory.
- **Data Type Handling:** Working with different data types and their representations.
- **Code Organization:** Structuring code for extensibility and maintainability.

---

## **📂 Project Structure**
```
ft_printf/
│── ft_print_charstr.c      # Character and string printing functions
│── ft_print_hexa.c         # Hexadecimal number printing functions
│── ft_print_int.c          # Integer printing functions
│── ft_print_percent.c      # Percent sign printing function
│── ft_print_ptr.c          # Pointer address printing functions
│── ft_print_unsigned.c     # Unsigned integer printing functions
│── ft_printf.c             # Main printf implementation
│── ft_printf.h             # Header file with function prototypes
│── Makefile                # Compilation instructions
```

---

## **🛠️ Installation & Usage**
To use the library in your projects, clone the repository and compile it.

### **📥 Clone & Compile**
```
git clone https://github.com/osmaneb23/42-printf.git
cd 42-printf
make
```

### **📌 Usage in Your Projects**
After compiling, link `libftprintf.a` when compiling your own C files:

```
# Method 1: Using library flags
gcc your_file.c -L. -lftprintf -o your_program

# Method 2: Directly specifying the library file
gcc your_file.c libftprintf.a -o your_program
```

### **📖 Function Usage**
```
#include "ft_printf.h"

int main(void)
{
    // Basic usage
    ft_printf("Hello, %s!\n", "world");
    
    // Multiple conversions
    ft_printf("Character: %c, String: %s, Integer: %d\n", 'A', "test", 42);
    
    // Hexadecimal and pointer
    int num = 255;
    ft_printf("Decimal: %d, Hex (lower): %x, Hex (upper): %X, Pointer: %p\n", 
              num, num, num, &num);
    
    // Return value (characters printed)
    int count = ft_printf("This printed %d characters\n", 0);
    ft_printf("Previous line printed %d characters\n", count);
    
    return (0);
}
```

---

## **📊 Function Return Values**
Similar to the original `printf()`, the `ft_printf()` function returns:
- The **number of characters printed** on success.
- **-1** if an error occurs.

---

## **⚠️ Limitations**
This implementation does not support:
- Buffer management like the original printf
- Format flags (width, precision, etc.)
- Length modifiers
- Other conversion specifiers not mentioned in requirements
