## Introduction
The **Libft** project is a fundamental project in the curriculum of many programming courses, particularly in those teaching the C programming language. In this project, students are tasked with creating their own library of essential functions in C. The goal is to gain a deeper understanding of C programming, standard library functions, and writing modular and reusable code.

## Project Overview 🚀
- **Objective**: Create a library of essential functions in C.
- **Purpose**: 
  - Reinforce understanding of C programming concepts.
  - Practice writing modular and reusable code.
  - Gain familiarity with standard library functions.
- **Key Components**:
  - Implementation of standard library functions (e.g., `strlen`, `strcpy`, `atoi`, etc.).
  - Additional utility functions (e.g., linked list manipulation, string manipulation, etc.).
- **Requirements**:
  - Functions must be implemented according to the project requirements.
  - Functions should be thoroughly tested to ensure correctness.

## Project Structure 📁
- **libft.h**: Header file containing function prototypes and necessary macros.
- **libft.a**: Compiled library file containing the implemented functions.
- **Source Files**: Implementation of individual functions.
- **Makefile**: Build script for compiling the library.

## Challenges and Learning 💡
- **Understanding Standard Library Functions**: Implementing functions similar to those found in the standard library requires a solid understanding of their behavior and implementation.
- **Memory Management**: Proper memory allocation and deallocation are crucial aspects of writing robust C code.
- **Modular Design**: Designing functions that are modular and reusable improves code readability and maintainability.
- **Testing**: Thoroughly testing each function is essential to ensure correctness and identify any potential issues.

## Conclusion 🎉
The libft project is a foundational exercise that helps students develop essential skills in C programming. By creating their own library of functions, students gain a deeper understanding of programming concepts, improve their coding abilities, and prepare themselves for more advanced projects and challenges.

## References
[Project](https://github.com/Unam3dd/Libft)

### Fun Part

```c
int	ft_atoi(char *str)
{
	long long			to_dec = 0;
	int				    neg = 1;

	while (!(*str ^ ' ') || (*str >= '\t' && *str <= '\r'))
		str = (char *)-~(unsigned long long)str; // Wtff dude
	while ((!(*str ^ '+') || !(*str ^ '-')))
		if (!(*str++ ^ '-'))
			neg = ~(neg - 1);
	while (*str >= '0' && *str <= '9')
		to_dec = (to_dec << 1) + (to_dec << 3) + (*str++ & 0xF);
	if (to_dec > 0x7FFFFFFF || to_dec > -0x80000000) return (0);
	return (to_dec * neg);
}
```
