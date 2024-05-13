# LIBFT

The Libft project was developed as a part of the curriculum at HIVE Helsinki, a coding school affiliated with the 42 network of coding schools headquartered in Paris.
My project successfully passed evaluation by three human evaluators, in addition to Moulinette (School 42's automated evaluator), achieving the maximum score of 125 points, including the bonus section.

## PART 1
Many of the functions of the project are re-implementations of existing functions found in existing c libraries.

### • isalpha
Checks if a character is an alphabetic character (a-z or A-Z).

### • isdigit
Checks if a character is a decimal digit (0-9).

### • isalnum
Checks if a character is alphanumeric (a-z, A-Z, or 0-9).

### • isascii
Checks if a character is a 7-bit ASCII character (0-127).

### • isprint
Checks if a character is a printable character (including space).

### • strlen
Calculates the length of a string (number of characters before the null terminator).

### • memset
Sets a block of memory to a specified value.

### • bzero
Clears a block of memory to zero.

### • memcpy
Copies a block of memory from one location to another.

### • memmove
Copies a block of memory, handling overlapping memory regions correctly.

### • strlcpy
Safely copies a C-string into a fixed-sized buffer, avoiding buffer overflow.

### • strlcat
Safely concatenates a C-string onto the end of another, avoiding buffer overflow.

### • toupper
Converts a character to its uppercase equivalent.

### • tolower
Converts a character to its lowercase equivalent.

### • strchr
Locates the first occurrence of a character in a string.

### • strrchr
Locates the last occurrence of a character in a string.

### • strncmp
Compares the first n characters of two strings.

### • memchr
Locates the first occurrence of a character in a block of memory.

### • memcmp
Compares two blocks of memory.

### • strnstr
Locates a substring within a string, with a specified maximum length.

### • atoi
Converts a string to an integer.

### • calloc
Allocates memory for an array of elements and initializes them to zero.

### • strdup
Duplicates a string by dynamically allocating memory and copying the string into it.


## PART 2
Additional functions are either absent from libc or found in it in a different form:
### • ft_substrAllocates (with malloc(3)) and returns a substring
from the string ’s’.
The substring begins at index ’start’ and is of
maximum size ’len’.
### • ft_strjoinAllocates (with malloc(3)) and returns a new
string, which is the result of the concatenation
of ’s1’ and ’s2’.


### • ft_strtrimAllocates (with malloc(3)) and returns a copy of
’s1’ with the characters specified in ’set’ removed
from the beginning and the end of the string.### • ft_splitAllocates (with malloc(3)) and returns an array
of strings obtained by splitting ’s’ using the
character ’c’ as a delimiter.  The array must end
with a NULL pointer.### • ft_itoaAllocates (with malloc(3)) and returns a string
representing the integer received as an argument.
Negative numbers must be handled.


### • ft_strmapiApplies the function ’f’ to each character of the
string ’s’, and passing its index as first argument
to create a new string (with malloc(3)) resulting
from successive applications of ’f’.

### • ft_striteriApplies the function ’f’ on each character of
the string passed as argument, passing its index
as first argument.  Each character is passed by
address to ’f’ to be modified if necessary.### • ft_putchar_fdOutputs the character ’c’ to the given file
descriptor.


### • ft_putstr_fdOutputs the string ’s’ to the given file
descriptor.
### • ft_putendl_fd
Outputs the string ’s’ to the given file descriptor
followed by a newline.### • ft_putnbr_fdOutputs the integer ’n’ to the given file
descriptor.



## BONUS PART
The bonus part consists of functions to manipulate lists. All of the following functions rely on the struct below, which is defined in the header file (libft.h):

```
typedef struct s_list
{
	void			*content;
	struct s_list	*next;
}					t_list;
```

### • t_lstnewAllocates (with malloc(3)) and returns a new node.
The member variable ’content’ is initialized with
the value of the parameter ’content’.  The variable
’next’ is initialized to NULL.### • ft_lstadd_frontAdds the node ’new’ at the beginning of the list.### • ft_lstsizeCounts the number of nodes in a list.### • ft_lstlastReturns the last node of the list.


### • ft_lstadd_backAdds the node ’new’ at the end of the list.### • ft_lstdeloneTakes as a parameter a node and frees the memory of
the node’s content using the function ’del’ given
as a parameter and free the node.  The memory of
’next’ must not be freed.### • ft_lstclearDeletes and frees the given node and every
successor of that node, using the function ’del’
and free(3).
Finally, the pointer to the list must be set to
NULL.


### • ft_lstiterIterates the list ’lst’ and applies the function
’f’ on the content of each node.

### • ft_lstmapIterates the list ’lst’ and applies the function
’f’ on the content of each node.  Creates a new
list resulting of the successive applications of
the function ’f’.  The ’del’ function is used to
delete the content of a node if needed.

* * *