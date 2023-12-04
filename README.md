# 42_cc00_libft
42 cursus, common core, rank 00, project libft

### What is libft?

Libft is an individual project at 42 that requieres us to re-create some standard C library functions for future projects, and have a deeper understanding of data structures and basic algorithms. At 42 we are not allowed to use some standard libraries on our projects, so we have to keep growing this libary with our own functions as we go farther in the program.

### What's in it?

There are 6 sections:

1.  **Functions "is":** Functions that check is a character belongs to a group: numbers, letters, printable, etc.
2.  **Functions "lst":** Functions that are used to manage a list.
3.  **Functions "mem":** Functions that perform actions from memory data (all kind of data).
4.  **Functions "put":** Functions that send stuff to files or stdout, etc.
5.  **Functions "str":** Functions that perform actions with strings ('\0' ended set of characters).
6.  **Functions "to":** Functions that changes the status or the type of data.
 

### Groups of functions
Function | Functions "is" 		| Functions "lst" 						| Functions "mem" 		| Functions "put" 		| Functions "str" 		| Functions "to"
:-----------: | :-----------: | :-----------: | :-----------: | :-----------:| :-----------:| :-----------:
0x00|							| 										| 							| 									| | 
0x01|[ft_isalnum](#ft_isalnum)	| 	[ft_lstadd_back](#ft_lstadd_back)	| [ft_bzero](#ft_bzero)		| [ft_putchar_fd](#ft_putchar_fd)	| [ft_split](#ft_split)		| [ft_atoi](#ft_atoi) 
0x02|[ft_isalpha](#ft_isalpha)	| 	[ft_lstadd_front](#ft_lstadd_front) | [ft_calloc](#ft_calloc)	| [ft_putstr_fd](#ft_putstr_fd)		| [ft_strchr](#ft_strchr)	| [ft_itoa](#ft_itoa) 
0x03|[ft_isascii](#ft_isascii)	| 	[ft_lstclear](#ft_lstclear)			| [ft_memset](#ft_memset)	| [ft_putendl_fd](#ft_putendl_fd)	| [ft_strdup](#ft_strdup)	| [ft_tolower](#ft_tolower)
0x04|[ft_isdigit](#ft_isdigit)	| 	[ft_lstdelone](#ft_lstdelone)		| [ft_memcpy](#ft_memcpy)	| [ft_putnbr_fd](#ft_putnbr_fd)		| [ft_striteri](#ft_striteri)| [ft_toupper](#ft_toupper)
0x05|[ft_isprint](#ft_isprint)	| 	[ft_lstlast](#ft_lstlast)			| [ft_memchr](#ft_memchr)	| 									| [ft_strjoin](#ft_strjoin)	|
0x06|       					| 	[ft_lstiter](#ft_lstiter)			| [ft_memcmp](#ft_memcmp)	| 									| [ft_strlcpy](#ft_strlcpy)	| 
0x07|							| 	[ft_lstmap](#ft_lstmap)				| [ft_memmove](#ft_memmove)	| 									| [ft_strlcat](#ft_strlcat)	| 
0x08|							| 	[ft_lstnew](#ft_lstnew)				| 							| 									| [ft_strlen](#ft_strlen)	| 
0x09|							| 	[ft_lstsize](#ft_lstsize)			|  							| 									| [ft_strmapi](#ft_strmapi)	| 
0x0a|							| 										|  							| 									| [ft_strncmp](#ft_strncmp)	| 
0x0b|							| 										|  							| 									| [ft_strnstr](#ft_strnstr)	| 
0x0c|							| 										|  							| 									| [ft_strrchr](#ft_strrchr)	| 
0x0d|							| 										| 							| 									| [ft_strtrim](#ft_strtrim)	| 
0x0e|							| 										|  							| 									| [ft_substr](#ft_substr)	| 
0x0f| | | | | |


## Functions "is"

## [ft_isalnum](libft/ft_isalnum.c)

`int        ft_isalnum(int c)`

Description | Param. 1st | Return Value
:-----------: | :-----------: | :-----------:
Check for an alphanumeric character; it is equivalent to ([ft_isalpha](#ft_isalpha) or [ft_isdigit](#ft_isdigit))| The character to test | 0 if the character tests false and 1 if the character tests true.

## [ft_isalpha](libft/ft_isalpha.c)

`int        ft_isalpha(int c)`

Description | Param. 1st | Return Value
:-----------: | :-----------: | :-----------:
Check for a alpabetic character, it is equivalent to ([ft_isupper](#ft_isupper)(c) or [ft_islower](#ft_islower)(c)) | The character to test | 0 if the character tests false and 1 if the character tests true.

## [ft_isascii](libft/ft_isascii.c)

`int        ft_isascii(int c)`

Description | Param. 1st | Return Value
:-----------: | :-----------: | :-----------:
Checks for an ASCII character, which is any character between 0 and octal 0177 inclusive | The character to test | 0 if the character tests false and 1 if the character tests true.

## [ft_isdigit](libft/ft_isdigit.c)

`int         ft_isdigit(int c)`

Description | Param. 1st | Return Value
:-----------: | :-----------: | :-----------:
Check for a digit (0 through 9) | The character to test | 0 if the character tests false and 1 if the character tests true.

## [ft_isprint](libft/ft_isprint.c)

`int        ft_isprint(int c)`

Description | Param. 1st | Return Value
:-----------: | :-----------: | :-----------:
Checks for any printable character including space| The character to test | 0 if the character tests false and 1 if the character tests true.

# Functions "lst"

## [ft_lstadd_back](libft/ft_lstadd_back_bonus.c)

`void        ft_lstadd_back(t_list **lst, t_list *new)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------:| :-----------:
Adds the 'new' element to the end of a list| A pointer addres to the first element of a list | A pointer to the new element to be added to the list | None.

## [ft_lstadd_front](libft/ft_lstadd_front_bonus.c)

`void        ft_lstadd_front(t_list **lst, t_list *new)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------:| :-----------:
Adds the 'new' element to the beguining of a list| A pointer addres to the first element of a list | A pointer to the new element to be added to the list | None.

## [ft_lstclear](libft/ft_lstclear_bonus.c)

`void         ft_lstclear(t_list **lst, void (*del)(void *))`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------:| :-----------:
Deletes and frees every element of a list, using 'del' function and free(). Pointer to the is is set to NULL | A pointer addres to the first element of a list | A pointer to the fuction used to delete the content of each list element| None.

## [ft_lstdelone](libft/ft_lstdelone_bonus.c)

`void          ft_lstdelone(t_list *lst, void (*del)(void *))`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------:| :-----------:
Deletes and frees an element of a list, using 'del' function and free(). Memory of next should not be freed. | A pointer addres to the element to be deleted | A pointer to the fuction used to delete the content of list element| None.

## [ft_lstlast](libft/ft_lstlast_bonus.c)

`t_list          *ft_lstlast(t_list *lst)`

Description | Param. 1st | Return Value
:-----------: | :-----------: | :-----------:
Returns the last element of a list | A pointer to the first element of a list | A pointer to last element of the list.

## [ft_lstiter](libft/ft_lstiter_bonus.c)

`void          ft_lstiter(t_list *lst, void (*f)(void *))`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------:| :-----------:
Iterates the list 'lst' and applies the function 'f' to the content of each element| A pointer addres to the first element of the list | A pointer to the fuction used to process the content of every element| None.

## [ft_lstmap](libft/ft_lstmap_bonus.c)

`t_list          *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *))`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------:| :-----------:
Iterates the list 'lst' and applies the function 'f' to the content of each element generating a new list. The 'del' function wil be used if allocation fails| A pointer addres to an element of the list | A pointer to the fuction used to iterate the list | A pointer to the fuction used to delete the content of list element (if needed) | The new list. NULL if allocation fails.

## [ft_lstnew](libft/ft_lstnew_bonus.c)

`t_list          *ft_lstnew(void *content)`

Description | Param. 1st | Return Value
:-----------: | :-----------: | :-----------:
Allocates the space and returns a new list element. Content is initialized with 'content' parameter. The 'next' variable is set to NULL | Content to be used on the new element | The new element

## [ft_lstsize](libft/ft_lstsize_bonus.c)

`int          ft_lstsize(t_list *lst)`

Description | Param. 1st | Return Value
:-----------: | :-----------: | :-----------:
Counts the number of elements of a list | A pointer to the first element of a list | Longitude of the list

## Functions "mem"

## [ft_bzero](libft/ft_bzero.c)

`void       *ft_bzero(void *s,  size_t n)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:
 Erases the data in the "n" bytes of the memory starting at the location pointed by "s" writing zeroes | The string on which to operate | The number of bytes | None.

## [ft_calloc](libft/ft_calloc.c)

`void       *ft_calloc(size_t count, size_t size)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:
 Allocates enough space for count objects that are size bytes of memory each, and returns a pointer to the allocated memory. The allocated memory is filled with bytes of value zero | Number of elements to be allocated | Size of elements | A pointer to the allocated memory, or NULL if the request fails.

## [ft_memset](libft/ft_memset.c)

`void       *ft_memset(void *s, int c, size_t len)`

Description | Param. 1st | Param. 2nd | Param. 3rd | Return Value
:-----------: | :-----------: | :-----------: | :-----------: | :-----------:
Fill with "len" bytes of "c" the memory of "s"| The string on which to operate | Value c (converted to an unsigned char) | The number of bytes | A pointer to the memory area s.


## [ft_memcpy](libft/ft_memcpy.c)

`void       *ft_memcpy(void *dst, const void *src, size_t n)`

Description | Param. 1st | Param. 2nd | Param. 3rd | Return Value
:-----------: | :-----------: | :-----------: | :-----------: | :-----------:
Copies n bytes from memory area src to memory of dst. The memory  areas  must  not  overlap.  Use [ft_memmove](#ft_memmove) if the memory areas do overlap.| Memory area dst | Memory area src | The number of bytes | A pointer to the memory area dst.

## [ft_memchr](libft/ft_memchr.c)

`void       *ft_memchr(const void *s, int c, size_t n)`

Description | Param. 1st | Param. 2nd | Param. 3rd | Return Value
:-----------: | :-----------: | :-----------: | :-----------: | :-----------:
Scans the initial n bytes of s for the first instance of c | Memory area s| A character to search | The number of bytes | A pointer to the matching byte or NULL if the character does not occur in the given memory area.

## [ft_memcmp](libft/ft_memcmp.c)

`void       *ft_memcmp(void *dst, const void *src, size_t n)`

Description | Param. 1st | Param. 2nd | Param. 3rd | Return Value
:-----------: | :-----------: | :-----------: | :-----------: | :-----------:
Compares byte string s1 against byte string s2 | Memory area s1| Memory area s2 | The number of bytes | < 0 if s1 is less than s2, > 0 if s1 is graeter than s2, = 0 if s1 is equal to s2.

## [ft_memmove](libft/ft_memmove.c)

`void       *ft_memmove(void *dst, const void *src, size_t len)`

Description | Param. 1st | Param. 2nd | Param. 3rd | Return Value
:-----------: | :-----------: | :-----------: | :-----------: | :-----------:
Copies len bytes from the memory of src to dst. Memories may overlap. First, the bytes in src are copied into a temporary array and then to dst.| Memory area dst | Memory ares arc | The number of bytes | A pointer to the memory area dst.

## Functions "put"

## [ft_putchar_fd](libft/ft_putchar_fd.c)

`void       ft_putchar_fd(char c, int fd)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:
Sends the character 'c' to the file descriptor | The character to be send | The file descriptor | None.

## [ft_putstr_fd](libft/ft_putstr_fd.c)

`void       ft_putstr_fd(char *s, int fd)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:
Sends the string 's' to the file descriptor | The string to be send | The file descriptor | None.

## [ft_putendl_fd](libft/ft_putendl_fd.c)

`void       ft_putendl_fd(char *s, int fd)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:
Sends the string 's' to the file descriptor, followed by an newline character | The string to be send | The file descriptor | None.

## [ft_putnbr_fd](libft/ft_putnbr_fd.c)

`void       ft_putnbr_fd(int n, int fd)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:
Sends the nunber 'n' to the file descriptor | The number to be send | The file descriptor | None.

## Functions "str"

## [ft_split](libft/ft_split.c)

`char **ft_split(char const *s, char c)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:
Allocates (with malloc) and returns  an array of strings obtained by splitting s using the character 'c' as a delimiter. The array must be ended by a NULL pointer|The string to be split |The delimiter character| The array of new strings result of the split. NULL if the allocation fails.

## [ft_strchr](libft/ft_strchr.c)

`char		*ft_strchr(const char *s, int c)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:
Locates the first occurrence of 'c' in the string pointed to by 's'. The terminating null character is considered to be part of the string, therefore if 'c' is '\0', locates the terminating '\0'| Pointer to string | Character to be located | A pointer to the first occurrence of the character c in the string or NULL if the character is not found.

## [ft_strdup](libft/ft_strdup.c) 
`char       *ft_strdup(const char *s))`

Description | Param. 1st | Return Values
:-----------: | :-----------: | :-----------:
Duplicate string s1. Memory  for  the new string is obtained with malloc, and can  be  freed with free | The string to duplicate| A pointer   to  the  duplicated  string.  NULL  if  insufficient  memory  was available.

## [ft_striteri](libft/ft_striteri.c) 

Description | Param. 1st | Param. 2nd | Param. 3rd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:| :-----------:
Applies the function 'f' to all the characters of a string, using the index as first argument. Every character is passed as a pointer allowing to be changed | The string to iterare | The function to apply to each character | None.


## [ft_strjoin](libft/ft_strjoin.c)

`char *ft_strjoin(char const *s1, char const *s2)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:
Allocates (with malloc) and returns a new string, result of the concatenation of s1 and s2 |The prefix string |The suffix string | The new string. NULL if the allocation fails.

## [ft_strlcpy](libft/ft_strlcpy.c)

`size_t     ft_strlcpy(char *dst, const char *src, size_t dstsize)`

Description | Param. 1st | Param. 2nd | Param. 3rd | Return Value
:-----------: | :-----------: | :-----------: | :-----------: | :-----------:
Copies up to dstsize - 1 characters from the NUL-terminated string src to dst, NUL-terminating the result| Destination array | String to be copied | Number of characters to be copied from src | Total length of the string to create (length of src).

## [ft_strlcat](libft/ft_strlcat.c)

`size_t     ft_strlcat(char *dst, const char *src, size_t size)`

Description | Param. 1st | Param. 2nd | Param. 3rd | Return Value
:-----------: | :-----------: | :-----------: | :-----------: | :-----------:
Concatenate the string src to the end of dst. It will concatenate at most size - strlen(dst) - 1 bytes, NUL-terminating the result | Destination array | String to be appended to dst | Maximum number of characters to be appended | The initial length of dst plus the length of src.

## [ft_strlen](libft/ft_strlen.c) 
`size_t     ft_strlen(const char *s)`

Description | Param. 1st | Return Values
:-----------: | :-----------: | :-----------:
Calculates the length of the string pointed to by s, excluding the terminating null byte ('\0')	| The string to calculate | Number of characters in the string pointed to by s.

## [ft_strmapi](libft/ft_strmapi.c)

`char *ft_strmapi(char const *s, char (*f)(unsigned int, char))`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:
Applies the function f to each character of the string passed as argument to create a new string (with malloc) resulting from successive applications of f |The string on which to iterate| The function to apply to each character| The string created from the successive applications of f. Returns NULL if the allocation fails.

## [ft_strncmp](libft/ft_strncmp.c)

`int	strncmp(const char *s1, const char *s2, size_t n)`

Description | Param. 1st | Param. 2nd | Param. 3rd | Return Value
:-----------: | :-----------: | :-----------: | :-----------: | :-----------:
Lexicographically compare the null-terminated strings s1 and s2, but not more than n characters. The comparison is done using unsigned characters | The fisrt string to compare | The second string to compare | The maximun number of character to use of each string to do the comparision | An integer greater than, equal to, or less than 0, according as the string s1 is greater than, equal to, or less than the string s2.

## [ft_strnstr](libft/ft_strnstr.c)

`char       *ft_strnstr(const char *haystack, const char *needle, size_t len)`

Description | Param. 1st | Param. 2nd | Param. 3rd | Return Value
:-----------: | :-----------: | :-----------: | :-----------: | :-----------:
Locate substring, where not more than 'len' characters are searched. Finds the first occurrence of the substring 'needle' in  the  string 'haystack'. The terminating null bytes ('\0') are not compared. | String to be scanned | The small string to be searched in 'haystack' string|The maximum amount of characters to be searched |A pointer to the first character of the first occurrence of little is returned. NULL if the substring is not found. If 'needle' is an empty string, 'haystack' is returned.


## [ft_strrchr](libft/ft_strrchr.c)

`char		*ft_strrchr(const char *s, int c)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:
Locates the last occurrence of 'c' in the string pointed to by 's'. The terminating null character is considered to be part of the string, therefore if 'c' is '\0', locates the terminating '\0'| Pointer to string | Character to be located | A pointer to the last occurrence of the character c in the string or NULL if the character is not found.


## [ft_strtrim](libft/ft_strtrim.c)

`char *ft_strjoin(char const *s1, char const *s2)`

Description | Param. 1st | Param. 2nd | Return Value
:-----------: | :-----------: | :-----------: | :-----------:
Allocates (with malloc) and returns a copy of the string given as argument without the characters specified in the set argument at the beginning and the end of the string|The string to be trimmed |The reference set of character to trim | The trimmed string. NULL if the allocation fails.


## [ft_substr](libft/ft_substr.c)
`char   *ft_substr(char const *s, unsigned int start, size_t len)`

Description | Param. 1st | Param. 2nd | Param. 3rd | Return Value
:-----------: | :-----------: | :-----------: | :-----------: | :-----------:
Allocates (with malloc) and returns a substring from the string given in argument. The substring begins at index 'start' and is of maximum size 'len'| The string from which create the substring | The start index of the substring in the string| The maximum length of the substring | The substring. NULL if the allocation fails.


## Functions "to"

## [ft_atoi](libft/ft_atoi.c)

`int        ft_atoi(const char *str)`

Description | Param. 1st | Return Value
:-----------: | :-----------: | :-----------:
Convert a string to a integer | The string to be converted to int | The converted value.

## [ft_itoa](libft/ft_itoa.c)

`char   ft_itoa(int n)`

Description | Param. 1st | Return Value
:-----------: | :-----------: | :-----------:
Allocates (with malloc) and returns a string representing the integer received as an argument. Negative numbers must be handled | The integer to convert | The string representing the integer. NULL if the allocation fails.

## [ft_tolower](libft/ft_tolower.c)

`int        ft_tolower(int c)`

Description | Param. 1st | Return Value
:-----------: | :-----------: | :-----------:
If the character passed as an argument is an uppercase, convert to lower| The character to convert | If c is a uppercase letter, returns its lowercase equivalent. Otherwise,  it  returns  c.

## [ft_toupper](libft/ft_toupper.c)

`int        ft_toupper(int c)`

Description | Param. 1st | Return Value
:-----------: | :-----------: | :-----------:
If the character passed as an argument is a lowercase, convert to upper| The character to convert | If c is a lowercase letter, returns its uppercase equivalent. Otherwise,  it  returns  c.

## Best libft github Testers
- Francinette https://github.com/xicodomingues/francinette.git
- https://github.com/y3ll0w42/libft-war-machine
- https://github.com/Tripouille/libftTester
- https://github.com/alelievr/libft-unit-test

## Best libft github alternatives
- https://github.com/raccoman/libft
- https://github.com/pbie42/libft42protected.git
- https://github.com/alanbarrett2/42-Libft.git
- https://github.com/HyewonKkang/Libft
- https://github.com/appinha/42cursus-00-Libft
- https://github.com/nickdotht/libft.git
- https://github.com/jraleman/open-libft.git
- https://github.com/psprawka/Libft.git
- https://github.com/42corozco/42_libft
- https://github.com/achrafelkhnissi/1337.git
- https://github.com/Sbk3824/Libft.git
- https://github.com/cacharle/libft
- https://github.com/fpetras/libft
