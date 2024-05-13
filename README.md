The Libft project was made as part of the curriculum of HIVE Helsinki coding school, part of the 42 network of coding school headquartered in Paris.

My project passed 3 human evaluators, Francinette and Moulinette (School 42's electronic evaluator).
It received the maximum 125 points, including a bonus part.

PART 1
Many of the functions of the projects are re-implementations of existing functions found in existing c libraries.  Namely:
• isalpha 
• isdigit 
• isalnum 
• isascii 
• isprint 
• strlen 
• memset 
• bzero
• memcpy 
• memmove 
• strlcpy 
• strlcat
• toupper 
• tolower 
• strchr 
• strrchr 
• strncmp 
• memchr 
• memcmp 
• strnstr 
• atoi
• calloc 
• strdup


PART 2
Additional functions are either absent libc or present in a different form:
• ft_substrAllocates (with malloc(3)) and returns a substring
from the string ’s’.
The substring begins at index ’start’ and is of
maximum size ’len’.
• ft_strjoinAllocates (with malloc(3)) and returns a new
string, which is the result of the concatenation
of ’s1’ and ’s2’.


• ft_strtrimAllocates (with malloc(3)) and returns a copy of
’s1’ with the characters specified in ’set’ removed
from the beginning and the end of the string.• ft_splitAllocates (with malloc(3)) and returns an array
of strings obtained by splitting ’s’ using the
character ’c’ as a delimiter.  The array must end
with a NULL pointer.• ft_itoaAllocates (with malloc(3)) and returns a string
representing the integer received as an argument.
Negative numbers must be handled.


• ft_strmapiApplies the function ’f’ to each character of the
string ’s’, and passing its index as first argument
to create a new string (with malloc(3)) resulting
from successive applications of ’f’.

• ft_striteriApplies the function ’f’ on each character of
the string passed as argument, passing its index
as first argument.  Each character is passed by
address to ’f’ to be modified if necessary.• ft_putchar_fdOutputs the character ’c’ to the given file
descriptor.


• ft_putstr_fdOutputs the string ’s’ to the given file
descriptor.
• ft_putendl_fd
Outputs the string ’s’ to the given file descriptor
followed by a newline.• ft_putnbr_fdOutputs the integer ’n’ to the given file
descriptor.



BONUS PART
The bonus part consists of functions to manipulate lists. All of the following functions rely on the struct below, which is defined in the header file (lift.h):

//////// typedef struct s_list
//////// {
////////   	void			*content;
////////	     struct s_list	*next;
//////// }					t_list;


• t_lstnewAllocates (with malloc(3)) and returns a new node.
The member variable ’content’ is initialized with
the value of the parameter ’content’.  The variable
’next’ is initialized to NULL.• ft_lstadd_frontAdds the node ’new’ at the beginning of the list.• ft_lstsizeCounts the number of nodes in a list.• ft_lstlastReturns the last node of the list.


• ft_lstadd_backAdds the node ’new’ at the end of the list.• ft_lstdeloneTakes as a parameter a node and frees the memory of
the node’s content using the function ’del’ given
as a parameter and free the node.  The memory of
’next’ must not be freed.• ft_lstclearDeletes and frees the given node and every
successor of that node, using the function ’del’
and free(3).
Finally, the pointer to the list must be set to
NULL.


• ft_lstiterIterates the list ’lst’ and applies the function
’f’ on the content of each node.

• ft_lstmapIterates the list ’lst’ and applies the function
’f’ on the content of each node.  Creates a new
list resulting of the successive applications of
the function ’f’.  The ’del’ function is used to
delete the content of a node if needed.